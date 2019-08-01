Vagrant.configure("2") do |config|
    config.vm.box = "ngocquyhoang/docker"
    config.vm.box_version = "0.0.1"
    config.vm.define "spa-server"
    config.vm.box_check_update = true

    config.vm.network "private_network", ip: "10.10.10.10"

    config.vm.synced_folder "./", "/home/vagrant/spa/"

    config.vm.provider "virtualbox" do |vb|
        vb.name = "spa-virtual-machine"
        vb.memory = "2048"
    end

    config.vm.provision "shell", inline: <<-SHELL
        sudo apt-get update && sudo apt-get -y upgrade
    SHELL
end
