# -*- mode: ruby -*-
# vi: set ft=ruby :

# $B%j%U%!%l%s%9(B 
# https://docs.vagrantup.com.
Vagrant.configure("2") do |config|

  config.vm.box = "centos7.2"
  config.vm.network "private_network", ip: "192.168.33.70"

  config.vm.define :simple do |simple|
    simple.vm.hostname = 'simple'
    # $B%2%9%HB&$K(Bansible$B$r%$%s%9%H!<%k(B
    config.vm.provision 'ansible_local' do |ansible|
      ansible.playbook = './playbook.yml'
    end
  end
end
