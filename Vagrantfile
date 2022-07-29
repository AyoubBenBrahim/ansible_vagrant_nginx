# -*- mode: ruby -*-
# vi: set ft=ruby :

$server_config = <<-SCRIPT

sudo dnf makecache

sudo dnf install python3

sudo python3 -m pip install --upgrade pip
pip3 install --upgrade setuptools

pip3 install ansible

SCRIPT

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

        # server.vm.provision "shell", inline: $server_config , privileged: false

        # server.vm.provision "ansible_local" do |ansible|
        #     ansible.playbook = "provisioning/playbook.yaml"
        #     ansible.inventory_path = "/vagrant/provisioning/inventory.yaml"
        #     ansible.install = false
        #     ansible.limit = "all"
        #   end

    end

end