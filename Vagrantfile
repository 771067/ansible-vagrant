# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
	config.vm.box      = "ubuntu/trusty64"
	config.vm.synced_folder "~/Dropbox/Projects/", "/projects/"
  config.vm.synced_folder "~/data/", "/data/"

	config.vm.network "private_network", ip: "192.168.0.101"

	config.vm.provision "ansible" do |ansible|
		ansible.playbook = "playbook.yml"
		ansible.inventory_path = "hosts"
	end

	config.vm.provider :virtualbox do |virtualbox|
		# allocate 1024 mb RAM
		virtualbox.customize ["modifyvm", :id, "--memory", "1024"]
		# allocate max 50% CPU
		virtualbox.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
	end
end