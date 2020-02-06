# Windows VM

Quick setup for a Windows 10 VM using Vagrant box [peru/windows-10-enterprise-x64-eval](https://app.vagrantup.com/peru/boxes/windows-10-enterprise-x64-eval) on Arch Linux

## Dependencies

```bash
yay -S --needed vagrant virt-manager qemu vde2 ebtables dnsmasq bridge-utils openbsd-netcat

# Start the libvirt service
sudo systemctl enable libvirtd.service
sudo systemctl start libvirtd.service

vagrant plugin install vagrant-libvirt
```

## Run

```bash
VAGRANT_DEFAULT_PROVIDER=libvirt vagrant up
```
