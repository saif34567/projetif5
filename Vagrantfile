# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/focal64"

   config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     #vb.gui = true
  
     # Customize the amount of memory on the VM:
     vb.memory = "2048"
     vb.cpus = "4"
   end

  

   config.vm.network "forwarded_port", guest: 80, host: 8080

  
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  
  # config.vm.network "private_network", ip: "192.168.33.10"


  # config.vm.network "public_network"

 
   config.vm.synced_folder ".", "/var/www/html"

  
  
  

  
   config.vm.provision "shell", path: "bootstrap.sh"
end
