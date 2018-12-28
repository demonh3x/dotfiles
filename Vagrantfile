# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provision "shell", inline: <<-SHELL
apt-get update
apt-get install -y language-pack-en
echo "LC_ALL=en_US.UTF-8" >> /etc/default/locale
echo "LANG=en_US.UTF-8" >> /etc/default/locale
  SHELL
  config.vm.provision "shell", path: "vagrant-setup.sh"
  config.vm.provision "shell", inline: <<-SHELL
chown -R vagrant:vagrant /home/vagrant
  SHELL

end
