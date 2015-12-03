# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "private_network", ip: "192.168.192.168"
  config.vm.synced_folder ".", "/app", type: "nfs", mount_options: ['nolock,vers=3,udp,noatime,actimeo=1']

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 2
    vb.memory = 2048
  end

  config.vm.provision :shell, inline: "sudo apt-get update"
  config.vm.provision :docker
  config.vm.provision :docker_compose, yml: "/app/docker-compose.yml", run: "always"

end
