# cowroot
Universal Android root tool based on CVE-2016-5195. Watch this space.

I've ported https://gist.github.com/scumjr/17d91f20f73157c722ba2aea702985d2 to Android arm32.

It patches getuid() to always return 0, which *should* cause su to allow root without prompting.

As of right now, it **doesn't work**, and makes the system unstable, causing crashes, reboots etc. - This gives me hope though, something must be on the right tracks.
