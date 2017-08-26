# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION ="2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.ssh.forward_agent = true
    config.ssh.username = "vagrant"
    config.ssh.username = "vagrant"


    config.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--cableconnected1", "on"]
      end

    config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
    end

   config.vm.define "ubuntu_vm", primary: true do |ubuntu_vm|
     ubuntu_vm.vm.network "private_network",  ip: "192.168.33.50"
     ubuntu_vm.vm.network "forwarded_port", guest: 80, host: 8080
     ubuntu_vm.vm.box = "bento/ubuntu-16.04"
   end

end
