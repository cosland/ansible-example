# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "database.vagrant"
  config.vm.network "private_network", ip: "192.168.8.11"

  config.vm.provider "virtualbox" do |vb|
    # vb.gui = true
    vb.memory = "1024"
  end

  config.vm.provision "ansible" do |a|
    a.playbook = "database.yml"
    # a.inventory_path = "inventories/development.ini"
    a.verbose = "vv"
  end

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"
end
