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






#    config.ssh.insert_key = true
#    config.ssh.insert_key = false
#    ansible_ssh_private_key_file= '~/.vagrant.d/insecure_private_key'
  # config.vm.define "dev_crm_db", primary: true do |dev_crm_db|
  #  dev_crm_db.vm.network "private_network",  ip: "192.168.33.45"
  # end

#  config.vm.box = "bento/centos-7.1"
#     config.vm.box = "bento/ubuntu-16.04"
#    ubuntu_vm.vm.box = "v0rtex/xenial64"
#     ubuntu_vm.vm.box = "ubuntu/xenial64"
#     ubuntu_vm.vm.box = "precise64"

#     config.vm.define "dev_crm_ci", primary: false do |dev_crm_ci|
#            dev_crm_ci.vm.network "private_network",  ip: "192.168.11.50"
#            config.vm.provider :virtualbox do |vb|
#                vb.customize ["modifyvm", :id, "--memory", "2048"]
#                vb.customize ["modifyvm", :id, "--cpus", "2"]
#            end
#          end

end
