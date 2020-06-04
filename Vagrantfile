# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.define "centos" do |centos|
    centos.vm.box = "generic/centos8"
    centos.vm.network "private_network", ip: "192.168.47.10"
  end

  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "generic/ubuntu2004"
    ubuntu.vm.network "private_network", ip: "192.168.47.11"
  end
end
