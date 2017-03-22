# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "fgrehm/trusty64-lxc"
  config.vm.box_url = "https://atlas.hashicorp.com/fgrehm/boxes/trusty64-lxc/versions/1.2.0/providers/lxc.box"


    config.vm.define "web1" do |web1|
      web1.vm.box = "fgrehm/trusty64-lxc"
        config.vm.provider :lxc do |web1, override|
          web1.container_name = "web1-vagrant"
          web1.customize 'network.type', 'veth'
          web1.customize 'network.link', 'lxcbr0'
        end
    end
  
  config.vm.define "web2" do |web2|
      web2.vm.box = "fgrehm/trusty64-lxc"
        config.vm.provider :lxc do |web2, override|
          web2.container_name = "web2-vagrant"
          web2.customize 'network.type', 'veth'
          web2.customize 'network.link', 'lxcbr0'
        end
    end


    config.vm.define "web3" do |web3|
      web3.vm.box = "fgrehm/trusty64-lxc"
        config.vm.provider :lxc do |web3, override|
          web3.container_name = "web3-vagrant"
          web3.customize 'network.type', 'veth'
          web3.customize 'network.link', 'lxcbr0'
        end
    end


    config.vm.define "db1" do |db1|
      db1.vm.box = "fgrehm/trusty64-lxc"
        config.vm.provider :lxc do |db1, override|
          db1.container_name = "db1-vagrant"
          db1.customize 'network.type', 'veth'
          db1.customize 'network.link', 'lxcbr0'
        end
    end


    config.vm.define "db2" do |db2|
      db2.vm.box = "fgrehm/trusty64-lxc"
        config.vm.provider :lxc do |db2, override|
          db2.container_name = "db2-vagrant"
          db2.customize 'network.type', 'veth'
          db2.customize 'network.link', 'lxcbr0'
        end
    end


end
