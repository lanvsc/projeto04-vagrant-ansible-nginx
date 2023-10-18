Vagrant.configure("2") do |config|
  #Configurando VM do Projeto 04
  config.vm.define:proj04 do |proj04_config|
    proj04_config.vm.box = "bento/ubuntu-22.04"
    proj04_config.vm.network "forwarded_port", guest: 80, host: 8080
    proj04_config.vm.network "public_network", ip: "192.168.100.155"
    proj04_config.vm.provision "shell", path: "script.sh"
    proj04_config.vm.synced_folder "site/" , "/var/www/html"
    proj04_config.vm.provider "virtualbox" do |v|
      v.gui = true
      v.memory = "1024"
      v.cpus = "1"
    end
  end
end