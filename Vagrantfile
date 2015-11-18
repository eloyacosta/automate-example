Vagrant.configure(2) do |config|
  config.vm.define "linux-vm" do |linux|
	linux.vm.box = "ubuntu/trusty64"
 	linux.vm.hostname = "linux-vm"
	linux.vm.network "forwarded_port", guest: 8080, host: 8080

  	# linux.vm.synced_folder "../data", "/vagrant_data"
  
	# Enable provisioning with a shell script. Additional provisioners such as
  	# Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  	# documentation for more information about their specific syntax and use.
 	# linux.vm.provision "shell", inline: <<-SHELL
  	#   sudo apt-get update
  	#   sudo apt-get install -y apache2
  	# SHELL
  end
end

