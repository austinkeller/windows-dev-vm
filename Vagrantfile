# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "peru/windows-10-enterprise-x64-eval"
  # For latest version, see https://app.vagrantup.com/peru/boxes/windows-10-enterprise-x64-eval
  config.vm.box_version = "20210602.01"

  config.vm.provider "virtualbox" do |v|
    # Don't use the gui so that we can remotely start the VM and rdp in
    v.gui = false
    v.memory = 5120
    v.cpus = 2
  end

  config.vm.synced_folder "data/", "C:\\\\Users\\\\vagrant\\\\data"
end
