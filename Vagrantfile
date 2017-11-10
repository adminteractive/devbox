Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.box_check_update = false
  config.vm.hostname = 'dev'

  config.vm.provider :virtualbox do |vb|
    vb.memory = 4096
    vb.cpus = 2
  end

  config.vm.provision :shell, :path => "provision/base.sh"
  config.vm.provision :shell, :path => "provision/docker.sh"
  config.vm.provision :shell, :path => "provision/docker-compose.sh"
  config.vm.provision :shell, :path => "provision/nodejs.sh", privileged: false
end
