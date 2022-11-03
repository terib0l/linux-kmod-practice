Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1604"
  config.vm.synced_folder "./workspace", "/home/vagrant/workspace"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y build-essential linux-headers-$(uname -r)
  SHELL
end
