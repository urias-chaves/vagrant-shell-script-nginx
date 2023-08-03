Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.synced_folder "nginx", "/var/www/html"
  config.vm.provision "shell", path:"installngnix.sh"
  # config.vm.provider "virtualbox" do |vb|
  #   vb.name = "vagrant-shell-script-nginx"
  # end
  config.vm.provision "shell", path:"installnginx.sh"
end
