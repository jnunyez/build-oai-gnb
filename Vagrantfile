Vagrant.configure("2") do |config|
    config.vm.define "oai-build"
    config.vm.box = "generic/rhel8"
    config.vm.provider :libvirt do |libvirt|
      libvirt.cpus = 4
      libvirt.memory = 2048

    end
    config.vm.provision :shell, path: "bootstrap"
end
