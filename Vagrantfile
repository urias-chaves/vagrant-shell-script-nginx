Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "192.168.100.45"
  config.vm.network "public_network", ip:"192.168.100.45"
  config.vm.synced_folder "nginx_site", "/var/www/html"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "vagrant-shell-script-nginx"
  end
  config.vm.provision "shell", path:"nginx.sh"
end
