# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.define "server" do |server|
        server.vm.provider "docker" do |d|
            d.build_dir = "server"
            d.name = "server"
            d.expose = ["2000"]
            d.ports = ["2000:2000" ]
            d.vagrant_vagrantfile = "host/Vagrantfile"
            d.force_host_vm=true
        end
    end

    config.vm.define "proxy" do |proxy|
        proxy.vm.provider "docker" do |d|
            d.build_dir = "proxy"
            d.name = "proxy"
            d.expose = ["3000"]
            d.ports = ["3000:3000" ]
            d.vagrant_vagrantfile = "host/Vagrantfile"
            d.link ("server:server")
            d.force_host_vm=true
        end
    end
    config.vm.network "private_network", ip: "192.168.50.4"
end
