# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.define "mysql-db" do |db|

      # configurar rede local da vm
      db.vm.network "public_network", :bridge => "eth0", ip: "192.168.1.237"

      # habilitar acesso porta do MySql
      db.vm.network "forwarded_port", guest: 3306, host: 3306

      #instalar my sql via comandos shell
      db.vm.provision "shell", path: "bootstrap.sh"
      
  end

end
