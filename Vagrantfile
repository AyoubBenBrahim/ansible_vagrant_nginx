# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "generic/debian9"
    config.vm.synced_folder ".", "/vagrant"

    config.vm.define "ansible" do |server|
        server.vm.hostname = "ansible"
        server.vm.network "private_network", ip: "192.168.42.100"
        server.vm.provider :virtualbox do |v|
            v.name = "ansible"
            v.memory = 2000
            v.cpus = 1
        end

    end

end