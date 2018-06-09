# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.network "forwarded_port", guest: 1433, host: 1433, host_ip: "127.0.0.1", id: "Sql Server"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "SQL2017"
    vb.memory = "4096"
  end

  config.vm.provision "shell", path: "install_mssql2017.sh"
end
