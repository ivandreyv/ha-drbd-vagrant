# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define "node1" do |vm1|
    vm1.vm.box = "ubuntu/jammy64"
    vm1.vm.hostname = "node1"
    vm1.vm.network "private_network", ip: "192.168.56.10"
    vm1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
    vm1.vm.disk :disk, size: "1GB", name: "extra_storage"
  end


  config.vm.define "node2" do |vm2|
    vm2.vm.box = "ubuntu/jammy64"
    vm2.vm.hostname = "node2"
    vm2.vm.network "private_network", ip: "192.168.56.11"
    vm2.vm.disk :disk, size: "1GB", name: "extra_storage"
    vm2.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end
  end


end
