+++
title = "Fixing OCSP Must Staple Error on Firefox"
date = "2022-06-26 21:43:40+05:30"
[taxonomies]
tags = [ "OCSP", "TLS" ]
+++

I have enabled [OCSP Must-Staple][1] on my TLS certificates that I get from Let's Encrypt for my
internal [LuCI web portal][4] for my OpenWrt router. However, I've been unable to access this
website for the past few months on Firefox. Considering this is an internal website, I didn't think
much about it, especially because it was working fine on Chromium.

I was browsing [a thread on Lobsters][2] when I came across the same issue. I've been was facing the
same issue. For some reason, I remembered that OCSP responses need to be fetched by the server. In
my case, I'm running LuCI on nginx.

I installed [AdGuard Home][3] on a RaspberryPi 4B a few months ago and created some firewall rules
in my router to intercept all DNS plaintext traffic and redirect it to my RaspberryPi. I went back
to my nginx configuration on my router and realized that I had set `option resolver` to a public DNS
IP. Once I changed the value to my RaspberryPi's IP, Firefox was able to open my LuCI website as
expected.

Looks like no major web browser except Firefox honors OCSP Must-Staple which is why my website kept
on working on Chromium. There was an issue open about this on the Chromium issue tracker but [it has
been closed][5] with the WONTFIX status. Interestingly, the Chromium project [has mentioned][6] in
their Chrome Security FAQ document that <q
cite="https://chromium.googlesource.com/chromium/src/+/HEAD/docs/security/faq.md#What_s-the-story-with-certificate-revocation">Stapled
OCSP with the Must Staple option (hard-fail if a valid OCSP response is not stapled to the
certificate) is a much better solution to the revocation problem than non-stapled OCSP.</q> {{
kaomoji(label="a kaomoji expressing facepalm", text="(ノ_<。)") }}

[1]: https://blog.cloudflare.com/high-reliability-ocsp-stapling/
[2]: https://lobste.rs/s/rpyuic/look_at_search_engines_with_their_own
[3]: https://github.com/AdguardTeam/AdGuardHome
[4]: https://openwrt.org/docs/guide-user/luci/luci.essentials
[5]: https://bugs.chromium.org/p/chromium/issues/detail?id=572734
[6]: https://chromium.googlesource.com/chromium/src/+/HEAD/docs/security/faq.md#What_s-the-story-with-certificate-revocation
