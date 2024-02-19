+++
title = "Writing Ansible Playbooks Is Tedious"
[taxonomies]
tags = [ "yaml", "ansible" ]
+++

This might sound insane but I bought a new desktop back in October 2022 and I
haven't been able to set it up since then. Although I was dealing with some
personal issues till the end of February 2023, I could've set up my desktop the
usual way (write and execute the usual commands like a boring sysadmin) after
February 2023 but I decided that I would use this opportunity to learn how to
use Ansible. I didn't really start writing Ansible playbooks after that though
and my desktop ate dust for several months.

I started learning Ansible in the beginning of August 2023 and since then, I
haven't finished installing and configuring my desktop. I recently finished
writing roles to install Arch Linux on my desktop with the caveat that the LUKS
community module doesn't support detached headers so I created a LUKS container
manually. I want to submit a patch to add support for detached headers in
[`community.crypto.luks_device`][1] in the near future when I'm comfortable with
Python.

I hope that writing these playbooks will help me build a (somewhat) declarative
configuration for installing and configuring Arch Linux, and possibly
[Alpine][2] and [Chimera Linux][3] in the future, but writing YAML for Ansible
feels tedious as hell. I've been vomiting YAML since the past few weeks and it
feels like I'm spending too much time on it.

Sure, there's [NixOS][4] but that's an entirely different can of worms that I
don't want to open unless there are major changes focused toward:

- easier onboarding experience (no, not by making GUI installers and
  recommending GNOME)
- reducing fragmentation and increasing cohesiveness of the project as a whole
  (are flakes still "experimental"? Has the new nix CLI command finally replaced
  the old set of commands?)
- vastly better documentation (no, the Nix DSL source code isn't documentation)

I've come across alternative configuration formats like [CUE][5] and [Dhall][6]
and I was wondering if they could reduce the tediousness of writing YAML for
Ansible. Consider role argument validation, a feature added in Ansible 2.11,
which seems like a great idea but the amount of YAML that you may need to write
for it will probably seem annoying. Would it be necessary if we used something
like CUE or Dhall?

[1]: https://docs.ansible.com/ansible/latest/collections/community/crypto/luks_device_module.html
[2]: https://alpinelinux.org/
[3]: https://chimera-linux.org/
[4]: https://nixos.org/
[5]: https://cuelang.org/
[6]: https://dhall-lang.org/
