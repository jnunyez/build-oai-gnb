Vagrant.configure("2") do |config|
    config.vm.define "oai-build"
    config.vm.box = "generic/rhel8"
    config.vm.provider :libvirt do |libvirt|
      libvirt.cpus = 4
      libvirt.memory = 2048
      libvirt.usb_controller :model => "nec-xhci"
      libvirt.usb :bus => "1", :device => "24", :vendor => "0x2500", :product => "0x0020"

    end
    config.vm.provision :shell, path: "bootstrap"
end
