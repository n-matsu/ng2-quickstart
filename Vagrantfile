Vagrant.configure(2) do |config|
	config.vm.box = "puphpet/centos65-x64/nvm_git"
	config.vm.network "forwarded_port", guest: 80, host: 8080
	config.vm.network "private_network",  ip: "192.168.33.10"
end
