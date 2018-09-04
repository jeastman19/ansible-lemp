# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.network "private_network", ip: "192.168.50.5"

  config.vm.provision "shell", inline: "which python || sudo apt -y install python"


  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
