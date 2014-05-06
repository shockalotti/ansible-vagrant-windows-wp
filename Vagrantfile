# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.require_version '>= 1.5.1'

Vagrant.configure("2") do |config|
  config.vm.box = 'stamm/precise64-docker'
  
  config.vm.network :private_network, ip: '192.168.50.10'
  
  config.vm.hostname = 'anisblewp.dev'
  
#  config.vm.synced_folder '../files', '/var/www/vhost', owner: 'vagrant', group: 'www-data', mount_options: ['dmode=776', 'fmode=775']
 
  config.vm.provision :shell do |sh|
    sh.path = "bootstrap.sh"
    sh.args = "./ansible provisioning/site.yml provisioning/hosts"
  end

end

