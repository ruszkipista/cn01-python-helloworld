# set up the default terminal
ENV["TERM"]="linux"

Vagrant.configure("2") do |config|
  config.vm.define "SUSEbox"
  # set the image for the vagrant box
  config.vm.box = "opensuse/Leap-15.2.x86_64"
  ## Set the image version
  # config.vm.box_version = "15.2.31.483"

  # set the static IP for the vagrant box
  config.vm.network "private_network", ip: "192.168.50.4"
  
  # configure the parameters for VirtualBox provider
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = 4
    vb.customize ["modifyvm", :id, "--ioapic", "on"]
  end
end
