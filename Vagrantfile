# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/centos-6.7"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.ssh.forward_agent = true
  config.vm.provision "chef_solo" do |chef|
    chef.add_recipe "springboot_petclinic"
  end
end
