# cowroot
Universal Android root tool based on CVE-2016-5195. Watch this space.

Current Status: Able to silently get root on Cyanogenmod devices, when both getuid() and geteuid() are patched.

I've ported https://gist.github.com/scumjr/17d91f20f73157c722ba2aea702985d2 to Android arm32.

As a proof-of-concept, it patches getuid() in libc to always return 0. Unless there is a su binary like on Cyanogenmod devices, this doesn't do anything useful.

In order to get "real" root, I'm going to have to use a different patching strategy.

If I patch a function that is used by an already-privileged process, I should be able to get full control.
