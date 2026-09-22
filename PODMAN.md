# mailcow: podmanized - 🐮 + 🦭 = 💕

What's needed to get this working:
* Podman needs a sock file, usually enabled via `systemctl enable --now podman.service podman.socket`
* podman-docker and docker-compose packages need to be installed via your favourite package manager.
* Only podman-compose 1.5+ (standalone) works. All other *compose solutions fail to interpret .env correctly.
* Podman 4+ required. Default network backend needs to be netavark, not CNI. CNI doesn't support DNS.

This is an attempt to get mailcow working on podman.
Results so far:
* All the containers (bar ipv6nat) come up and communicate with each other.
* Only master branch is supported.
* Watchdog is disabled via generate_config.sh as it causes containers to constantly restart due to timeouts.

Kudos to the mailcow team, show your support by visiting their repo.

