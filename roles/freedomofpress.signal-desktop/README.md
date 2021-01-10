Signal Desktop Ansible role
===========================

Installs [Signal Desktop] on Linux hosts via `apt`.

Requirements
------------

Debian or Ubuntu.

Role Variables
--------------

```yaml
# GPG full fingerprint of apt repo key, retrieved from:
# https://updates.signal.org/desktop/apt/keys.asc
signal_desktop_gpg_fingerprint: "DBA36B5181D0C816F630E889D980A17457F6FB06"

# Prerequisites for configuring HTTPS apt repo.
signal_desktop_apt_dependencies:
  - apt-transport-https
  - gpg

# Pinning the Xenial repo, works fine on e.g. Debian Stretch.
# The Signal team does not maintain specific versions for other dists,
# so intentionally not using `{{ ansible_distribution }}`
signal_desktop_apt_repo: "deb [arch=amd64] https://updates.signal.org/desktop/apt xenial main"
```



Example Playbook
----------------

```yaml
- hosts: workstations
  roles:
    - role: freedomofpress.signal-desktop
```

License
-------

MIT
