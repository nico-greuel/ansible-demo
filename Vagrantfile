# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "256"]
  end

  # App Server 1
  config.vm.define "app1" do |app|
    app.vm.hostname = "app1.dev"
    app.vm.box = "geerlingguy/centos7"
    app.vm.network :private_network, ip: "192.168.60.11"
  end

  # App Server 2
  config.vm.define "app2" do |app|
    app.vm.hostname = "app2.dev"
    app.vm.box = "geerlingguy/centos7"
    app.vm.network :private_network, ip: "192.168.60.12"
  end

  # Database Server
  config.vm.define "db1" do |app|
    app.vm.hostname = "db1.dev"
    app.vm.box = "geerlingguy/centos7"
    app.vm.network :private_network, ip: "192.168.60.21"
  end

  config.vm.box = "geerlingguy/centos7"

end
