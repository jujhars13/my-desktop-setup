# My Desktop Setup
My ~~Ubuntu~~ desktop base setup using Ansible. Tested using Vagrant

- ~~Ubuntu (20)~~ Ubuntu 24.04 LTS (Noble Numbat)
- Fedora (35)

## Usage

To install on vanilla setup use with `ansible-pull` to initialise a local install:

```bash
# on Ubuntu
sudo apt-get update && sudo apt-get install -y ansible git

# on Fedora
sudo dnf install -y ansible git

# then
sudo ansible-pull --url https://github.com/jujhars13/my-desktop-setup.git
```

## Testing

Test in a Vagrant VM:

```bash
# Ubuntu
vagrant destroy -f && vagrant up

# Fedora
VAGRANT_VAGRANTFILE=Vagrantfile.fedora vagrant destroy -f && vagrant up
```

## Inspired by

- https://github.com/lvancrayelynghe/ansible-ubuntu
- https://github.com/awailly/cis-ubuntu-ansible
- https://github.com/davestephens/ansible-nas
