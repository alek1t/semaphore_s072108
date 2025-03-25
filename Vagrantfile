# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "master_node" do |master_node|
    master_node.vm.box = "almalinux/8"
    master_node.vm.hostname = "masternode"
    master_node.vm.network "private_network", ip: "192.168.50.4"
    master_node.vm.synced_folder "./gitlab_ansible_course", "/home/vagrant/gitlab_ansible_course", type: "virtualbox"
    master_node.vm.provision "shell", inline: <<-SHELL
      sed -i 's/ChallengeResponseAuthentication no/ChallengeResponseAuthentication yes/#g' /etc/ssh/sshd_config
      service sshd restart
    SHELL
  end

  config.vm.define "slave_node" do |slave_node|
    slave_node.vm.box = "almalinux/8"
    slave_node.vm.hostname = "slavenode"
    slave_node.vm.network "private_network", ip: "192.168.50.5"
    slave_node.vm.provision "shell", inline: <<-SHELL
      sed -i 's/ChallengeResponseAuthentication no/ChallengeResponseAuthentication yes/#g' /etc/ssh/sshd_config
      service sshd restart
    SHELL
  end

end
