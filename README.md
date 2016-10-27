# cowroot
Universal Android root tool based on CVE-2016-5195. Watch this space.

I've ported https://gist.github.com/scumjr/17d91f20f73157c722ba2aea702985d2 to Android arm32.

As a proof-of-concept patches getuid() in libc to always return 0. Because of SELinux, this doesn't give us "real" root access.

In order to get "real" root, I'm going to have to use a different patching strategy.

If I patch a function that is used by an alread-privilidged process, I should be able to get full control.
