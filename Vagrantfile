# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian9"
  config.vm.guest = :linux

  #config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt install qemu-kvm libvirt-clients libvirt-daemon-system
    wget -q https://releases.hashicorp.com/packer/1.1.3/packer_1.1.3_linux_amd64.zip
    unzip packer_1.1.3_linux_amd64.zip
  SHELL
end
