See https://github.com/renovatebot/renovate/discussions/27806

- The source tree exposes 2 Dockerfiles, one in each subdir.
- Both Dockerfiles uses an image following the <codename>-<date> format, but one is Debian, the other is Ubuntu
- Both images are slightly outdated and can be updated
- The same Renovate conf is used for both except the debian versioning scheme is used for Debian, and the ubuntu versioning scheme is used for Ubuntu

Running Renovate on this will only open an MR for Ubuntu, and won't detect the version for Debian.
