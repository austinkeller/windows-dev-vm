# Windows VM

Quick setup for a Windows 10 VM using Vagrant box
[peru/windows-10-enterprise-x64-eval](https://app.vagrantup.com/peru/boxes/windows-10-enterprise-x64-eval)
on Arch Linux

## Dependencies

```bash
yay -S --needed vagrant virtualbox
```

## Run

To initialize the box from scratch, run:

```bash
VAGRANT_DEFAULT_PROVIDER=virtualbox vagrant up
```

Once initialized, the box can be managed from `virtualbox`, including
starting if in a suspended state. To use the machine, you can open a viewer
window by double-clicking on the entry in `virtualbox`. Alternatively, you
can use RDP to access the machine by running

```bash
vagrant rdp
```
