
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "CentOS1706_v0.2.0"
  config.vm.provision :chef_solo do |chef|
    chef.install = false
    chef.cookbooks_path = "cookbooks"
    chef.add_recipe "httpd"
    config.vm.network "forwarded_port", guest: 80, host: 8080
  end  
end
