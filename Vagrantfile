# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "server_centos" do |server_centos|
    server_centos.vm.box = "C:/Users/Defaultpc/Desktop/Study/practice/CentOS-7.box"
    server_centos.vm.hostname = "centos"
    server_centos.vm.network "private_network", ip: "192.168.56.42"
    server_centos.vm.synced_folder "C:/Users/Defaultpc/Desktop/Study/practice/ansible", "/home/vagrant/ansible"

    server_centos.vm.provision "file", source: "C:/Users/Defaultpc/Desktop/Study/practice/files/vagrant_new_key", destination: "/home/vagrant/.ssh/vagrant_new_key"
    server_centos.vm.provision "file", source: "C:/Users/Defaultpc/Desktop/Study/practice/files/vagrant_new_key.pub", destination: "/home/vagrant/.ssh/vagrant_new_key.pub"
  end
end
