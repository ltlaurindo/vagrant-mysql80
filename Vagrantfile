# -- mode: ruby --
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define "mysql" do |node|
    config.vm.box = "jitendradpatel/mysql-8"
    config.vm.network "forwarded_port", guest: 3306, host: 3306
    node.vm.network "public_network"
    node.vm.provider "virtualbox" do |vb|
      vb.name = "mysql"
      vb.memory = "1024"
      vb.cpus = 1
    end
    config.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y apache2
    SHELL
  end
end