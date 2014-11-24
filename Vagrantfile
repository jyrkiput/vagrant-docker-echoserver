# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.provider "docker" do |d|
        d.build_dir = "server"
        d.expose = ["2000"]
        d.ports = ["2000:2000" ]
        d.vagrant_vagrantfile = "host/Vagrantfile"
    end
    config.vm.network "private_network", ip: "192.168.50.4"
end
