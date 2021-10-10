# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
    # Plantilla "ArchLinux".
    config.vm.box = "archlinux/archlinux"
    # Nombre de la máquina.
    config.vm.hostname = "My_Arch"

    # Configuración
    config.vm.provider :virtualbox do |vb|
        # Nombre del hostname.
        vb.customize [ 'modifyvm', :id, '--name', 'My_Arch' ]
        # Cantidad de cores.
        vb.customize [ 'modifyvm', :id, '--cpus', '1' ]
        # Cantidad de RAM.
        vb.customize [ 'modifyvm', :id, '--memory', '1024' ]
        # Cantidad VRAM.
        vb.customize [ 'modifyvm', :id, '--vram', '64' ]

    config.vm.provision "shell", path: "software.sh"
    end
end