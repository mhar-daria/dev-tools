# Dev Tools
Basic commads

## Amazon Linux AMI 2 - NGINX Installation
```
  sudo amazon-linux-extras install nginx1.12
```

## Amazon Linux AMI 2 - PHP 7.2 Installation
```
  sudo yum -y install epel-release
  sudo yum-config-manager --enable remi-php72
  sudo amazon-linux-extras install php7.2
  sudo yum -y install php-xml php-cli php-mcrypt php-json php-gd
```

## CodeDeploy Installation
```
  sudo yum update && sudo yum upgrade
  sudo yum install wget
  wget https://aws-codedeploy-ap-southeast-1.s3.amazonaws.com/latest/install
  sudo yum install ruby
  chmod +x install
  sudo ./install auto
  sudo service codedeploy-agent status
```

### Install Composer
```
  cd ~
  sudo curl -sS https://getcomposer.org/installer | sudo php
  sudo mv composer.phar /usr/local/bin/composer
  sudo ln -s /usr/local/bin/composer /usr/bin/composer
  composer -v
```
