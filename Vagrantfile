Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provision :shell, :path => "provision-ubuntu-16.04.sh"
  config.vm.network "private_network", ip: "192.168.56.101"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--cpuexecutioncap", "95", "--cpus", "1"]
    vb.memory = 2048
  end

  config.vm.synced_folder ".", "/vagrant", owner: "www-data", group: "ubuntu"
end