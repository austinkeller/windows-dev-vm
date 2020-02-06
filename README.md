# Windows VM

Quick setup for a Windows 10 VM using Vagrant box
[peru/windows-10-enterprise-x64-eval](https://app.vagrantup.com/peru/boxes/windows-10-enterprise-x64-eval)
on Arch Linux

## Dependencies

```bash
yay -S --needed vagrant virt-manager qemu vde2 ebtables dnsmasq bridge-utils openbsd-netcat

# Start the libvirt service
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service

vagrant plugin install vagrant-libvirt
```

## Run

To initialize the box from scratch, run:

```bash
VAGRANT_DEFAULT_PROVIDER=libvirt vagrant up
```

Once initialized, the box can be managed from `virt-manager`, including
starting if in a suspended state. To use the machine, you can open a viewer
window by double-clicking on the entry in `virt-manager`. Alternatively, you
can use RDP to access the machine by running

```bash
rdesktop -u vagrant -p vagrant $(vagrant ssh-config | grep HostName | sed 's/^[[:space:]]*//' | cut -d' ' -f2):3389
```
