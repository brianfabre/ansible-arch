**Forked from [loganmarchione/ansible-arch-linux](https://github.com/loganmarchione/ansible-arch-linux/)**

# ansible-arch-linux

Ansible playbook to setup my own personal Arch Linux machines (i.e., meant to be run against localhost)

## Explanation

* This is meant for _my machine_. You can use it as a guide, but please don't blindly run it on your machine (it will break things).
* This is meant to be run in the [Post-installation](https://wiki.archlinux.org/title/installation_guide#Post-installation) section of the [Installation guide](https://wiki.archlinux.org/title/installation_guide) (i.e., after your partitions are setup, user account is created, fstab is setup, chroot, etc...)

## Requirements

1. Install the necessary packages
   ```
   sudo pacman -S ansible git python
   ```
1. Clone this repo
   ```
   git clone https://github.com/brianfabre/ansible-arch.git
   cd ansible-arch
   ```
1. Install the Ansible requirements
   ```
   ansible-galaxy install -r requirements.yml
   ```
1. Edit the variables in `group_vars`
1. (Optional) Run the playbook in check mode to view potential changes
   ```
   ansible-playbook main.yml --ask-become-pass --check
   ````
1. Run the playbook (enter your user's password when prompted)
   ```
   ansible-playbook main.yml --ask-become-pass
   ```
