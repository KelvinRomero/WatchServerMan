# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.synced_folder "./", "/var/www/html"

  config.vm.provision "shell", inline: <<-SHELL
   echo "System update"
    sudo locale-gen UTF-8 > /dev/null
    sudo apt-get install -y language-pack-en-base > /dev/null
    sudo LC_ALL=en_US.UTF-8 add-apt-repository ppa:ondrej/php -y > /dev/null
    sudo apt-get -y update > /dev/null

    echo "Installing Apache"
    sudo apt-get -y install apache2 > /dev/null

    echo "Installing PHP"
    sudo apt-get -y install php5.5 > /dev/null # mod_php
    echo '<?php phpinfo(); ?>' | sudo tee --append /var/www/html/info.php  > /dev/null

    sudo service apache2 restart > /dev/null
    echo "Finish Installing LAMP!!!"
    echo "Open http://localhost:8000"
  SHELL
end
