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

  config.ssh.insert_key = false
  config.ssh.private_key_path = [
    './id_ed25519-rga_demo',
    '~/.vagrant.d/insecure_private_key'
  ]
  config.vm.provision 'file',
    source: './id_ed25519-rga_demo.pub',
    destination: '~/.ssh/authorized_keys'
end
