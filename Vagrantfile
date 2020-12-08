Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.provision "shell", inline: <<-SHELL
      sudo apt -y update
      sudo apt -y install gcc
      sudo apt -y install libreadline-dev
      sudo apt -y install zlibc zlib1g-dev
      sudo apt -y install make 
      wget https://ftp.postgresql.org/pub/source/v8.4.22/postgresql-8.4.22.tar.gz
      gunzip postgresql-8.4.22.tar.gz
      tar xf postgresql-8.4.22.tar
      cd postgresql-8.4.22/
      ./configure
      sudo make
      sudo make install
   SHELL
end
