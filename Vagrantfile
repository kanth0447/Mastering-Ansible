# -*- mode: ruby -*-
# vi: set ft=ruby :

# README
#
# Getting Started:
# 1. vagrant plugin install vagrant-hostmanager
# 2. vagrant up
# 3. vagrant ssh
#
# This should put you at the control host
#  with access, by name, to other vms
Vagrant.configure(2) do |config|
  config.hostmanager.enabled = true

  config.vm.box = "bento/ubuntu-18.04"

  config.vm.define "lb01" do |h|
    h.vm.network "private_network", ip: "192.168.125.201"
    h.vm.hostname = "lb01"
  end

  config.vm.define "app01" do |h|
    h.vm.network "private_network", ip: "192.168.125.211"
    h.vm.hostname = "app01"
  end

  config.vm.define "app02" do |h|
    h.vm.network "private_network", ip: "192.168.125.212"
    h.vm.hostname = "app02"
  end

  config.vm.define "db01" do |h|
    h.vm.network "private_network", ip: "192.168.125.221"
    h.vm.hostname = "db01"
  end
end
