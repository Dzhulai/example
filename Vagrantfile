# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "CentOS"
  config.vm.hostname = "build-server"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.100.10"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.yml"
    ansible.sudo = true
  end
end