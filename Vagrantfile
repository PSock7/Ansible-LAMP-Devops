# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Common configuration options for both VMs.

  config.vm.box = "geerlingguy/centos7"
  config.vm.network "public_network", bridge: "#$default_network_interface"

  # Ansible Controller configuration.
  config.vm.define "ansible-controller" do |ansible_controller|
    ansible_controller.vm.network "private_network", ip: "192.168.38.30"
    # Additional Ansible Controller specific configurations if needed.
  end

  # Ansible Target configuration.
  config.vm.define "ansible-target" do |ansible_target|
    ansible_target.vm.network "private_network", ip: "192.168.34.15"
    # Additional Ansible Target specific configurations if needed.
  end

  # Additional shared configurations if needed.

  # Example Provider-specific configuration for VirtualBox:
  # config.vm.provider "virtualbox" do |vb|
  #   vb.gui = true
  #   vb.memory = "1024"
  # end

  # Example provisioning with shell scripts for each VM.
  # Uncomment and customize as needed.
  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y apache2
  # SHELL
end
