Vagrant.configure("2") do |config|
	config.vm.box = "hashicorp/precise32"

	config.vm.define :db do |db_config|
		db_config.vm.hostname = "db"
		db_config.vm.network :private_network, :ip => "192.168.33.10"

		db_config.vm.provision "shell", path: "provisioning/conf/ansible-boot.sh"
		db_config.vm.provision "ansible" do |ansible|
			ansible.playbook = "provisioning/db.yml"
		end
	end

	config.vm.define :web do |web_config|
		web_config.vm.hostname = "web"
		web_config.vm.network :private_network, :ip => "192.168.33.12"
		
		web_config.vm.provision "shell", path: "provisioning/conf/ansible-boot.sh"
		web_config.vm.provision "ansible" do |ansible|
			ansible.playbook= "provisioning/web.yml"
		end
	end
   
	config.vm.define :monitor do |monitor_config|
		monitor_config.vm.hostname = "monitor"
		monitor_config.vm.network :private_network, :ip => "192.168.33.14"
		
		monitor_config.vm.provision "shell", path: "provisioning/conf/ansible-boot.sh"
		monitor_config.vm.provision "ansible" do |ansible|
			ansible.playbook= "provisioning/monitor.yml"
		end
	end
end
