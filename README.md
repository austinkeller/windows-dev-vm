# Windows VM

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
