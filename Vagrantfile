# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "peru/windows-10-enterprise-x64-eval"
  # For latest version, see https://app.vagrantup.com/peru/boxes/windows-10-enterprise-x64-eval
  config.vm.box_version = "20200501.01"

  config.vm.provider "virtualbox" do |v|
    # Don't use the gui so that we can remotely start the VM and rdp in
    v.gui = false
  end

  config.vm.synced_folder "data/", "C:\\\\Users\\\\vagrant\\\\data"
  config.vm.provision "shell", path: "scripts/install_certs.ps1"
end
