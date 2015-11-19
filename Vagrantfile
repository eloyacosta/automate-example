# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "linux-vm" do |linux|
	linux.vm.box = "ubuntu/trusty64"
 	linux.vm.hostname = "linux-vm"
	
	#linux.vm.network "forwarded_port", guest: 8080, host: 8080
	linux.vm.network :private_network, ip: "192.168.100.2"


  	# linux.vm.synced_folder "../data", "/vagrant_data"

    	linux.vm.provision "ansible" do |ansible|
		ansible.inventory_path = "provision/inventory"
        	ansible.playbook = "provision/playbook.yml"
    		#ansible.sudo = true
    	end  
  end
end
