Vagrant.configure("2") do |config|
    config.vm.box = "naelyn/ubuntu-trusty64-libvirt"
    config.vm.synced_folder "salt/", "/srv/salt/"
    config.vm.synced_folder "pillar/", "/srv/pillar/"
    config.vm.synced_folder "formulas/", "/srv/formulas/"
    config.vm.provision :salt do |salt|
        salt.minion_config = "config/vagrant/minion"
        salt.run_highstate = true
    end
end
