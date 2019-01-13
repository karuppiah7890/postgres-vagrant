# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provision "shell", path: "create-postgres-user.sh"
  config.vm.synced_folder "postgresql-11.1", "/postgresql-11.1", automount: true
  config.vm.synced_folder "postgres-build-dir", "/postgres-build-dir", create: true, automount: true
  # config.vm.synced_folder "postgres-data-dir", "/postgres-data-dir", create: true, automount: true, owner: "postgres", group: "postgres"
end
