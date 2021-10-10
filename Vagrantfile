# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "archlinux/archlinux"
    config.vm.hostname = "My_Arch"
    config.vm.provider :virtualbox do |vb|
        vb.customize [ 'modifyvm', :id, '--name', 'My_Arch' ]
        vb.customize [ 'modifyvm', :id, '--cpus', '1' ]
        vb.customize [ 'modifyvm', :id, '--memory', '1024' ]
    config.vm.provision "shell", path: "software.sh"
    end
end