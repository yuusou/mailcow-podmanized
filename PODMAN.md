# mailcow: podmanized - 🐮 + 🦭 = 💕

What's needed to get this working:
* Podman needs a sock file, usually enabled via `systemctl --enable now podman.service podman.socket`
* podman-docker and docker-compose packages need to be installed via your favourite package manager.
* Podman 4+ required. Default network backend needs to be netavark, not CNI. CNI doesn't support DNS.

This is an attempt to get mailcow working on podman.
Results so far:
* IPv6 disabled and won't be supported for the time being. The ipv6nat container keeps crashing anyway.
* All the containers (bar ipv6nat) come up and communicate with each other.
* Only master branch is supported.

Kudos to the mailcow team, show your support by visiting their repo.

