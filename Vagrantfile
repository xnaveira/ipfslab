# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.define "ipfs" do |spine|
  config.vm.network "forwarded_port", guest: 5001, host: 5001
  config.vm.network "forwarded_port", guest: 8080, host: 8080
    spine.vm.box = "ubuntu/xenial64"
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ipfs_playbook.yaml"
    end
  end
end
