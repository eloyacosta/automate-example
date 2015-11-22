# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  
  config.vm.define "linux-vm" do |linux|
      
      linux.vm.box = "ubuntu/trusty64"
        
      linux.vm.provider "virtualbox" do |v|
          v.memory = 1024
          v.cpus = 2
      end
 	    
      linux.vm.hostname = "linux-vm"
      linux.vm.network :private_network, ip: "192.168.100.2"
      linux.vm.provision "ansible" do |ansible|
	      	ansible.inventory_path = "provisioning/inventory"
        	ansible.playbook = "provisioning/playbook.yml"
      end  
  end
end



