+++
title = "cargo-update Is Slow, Doesn't Respect XDG"
[taxonomies]
tags = [ "rust" ]
+++

I tried to install [greetd][1] from the Arch AUR but, suprisingly, a cargo registry update started
happening at less than 100Kbps on my 200Mbps fiber connection. I waited for a few minutes hoping
that the speed might improve but that didn't happen. It seems this is a [known issue][2]. Okay, I
guess I just need to create a config file for cargo and tell it use to `git-fetch-with-cli = true`.
Wait, it seems like cargo is dumping all of its crap inside `~/.cargo`? You can change the location
of this directory with the `$CARGO_HOME` environment variable but does it really make sense to dump
this data in `$XDG_CONFIG_HOME`? `$XDG_DATA_HOME`? [This issue][3] has been open for more than 5
years now.

I guess I'll just set `$CARGO_HOME` to `$(mktemp -d)` for now. If you want to compile a rust
software on your system, you may need this in `$CARGO_HOME/config.toml`

```
[net]
git-fetch-with-cli = true

[source.crates-io]
registry = "git://github.com/rust-lang/crates.io-index.git"
```

[1]: https://git.sr.ht/~kennylevinsen/greetd
[2]: https://github.com/rust-lang/cargo/issues/9167
[3]: https://github.com/rust-lang/cargo/issues/1734
