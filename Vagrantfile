ENV["LC_ALL"] = "en_US.UTF-8"
Vagrant.configure(2) do |config|
  config.vm.box = "centos72"
  config.vm.box_check_update = false
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["setextradata", :id, "VBoxInternal/Devices/VMMDev/0/Config/GetHostTimeDisabled", 0]
    vb.memory = 2048
    vb.cpus = 1
    vb.customize [
      "modifyvm", :id,
      "--hwvirtex", "on",
      "--nestedpaging", "on",
      "--largepages", "on",
      "--ioapic", "on",
      "--pae", "on",
      "--paravirtprovider", "kvm",
    ]
  end
end
