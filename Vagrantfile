# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "generic/debian9"
    config.vm.synced_folder ".", "/vagrant"

    config.vm.define "machine1" do |server|
        server.vm.hostname = "machine1"
        server.vm.network "private_network", ip: "192.168.42.100"
        server.vm.provider :virtualbox do |v|
            v.name = "machine1"
            v.memory = 2000
            v.cpus = 1
        end
    end

    config.vm.define "machine2" do |server|
        server.vm.hostname = "machine2"
        server.vm.network "private_network", ip: "192.168.42.110"
        server.vm.provider :virtualbox do |v|
            v.name = "machine2"
            v.memory = 2000
            v.cpus = 1
        end
    end

    config.vm.define "machine3" do |server|
        server.vm.hostname = "machine3"
        server.vm.network "private_network", ip: "192.168.42.120"
        server.vm.provider :virtualbox do |v|
            v.name = "machine3"
            v.memory = 2000
            v.cpus = 1
        end
    end

end