Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1604"
  config.vm.synced_folder "./workspace", "/home/vagrant/workspace"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y build-essential
    echo "Section2"
    cd /home/vagrant/workspace/kmod/hello
    make
    insmod ./hello.ko
    dmesg | tail -n 5
    rmsmod hello
    dmesg | tail -n 5
    make clean
    echo "Section4"
    cd /home/vagrant/workspace/kmod/jprobe
    make
    insmod ./jprobe.ko && dmesg && tail -n 3
    
    rmsmod jprobe && dmesg && tail -n 3
    make clean
  SHELL
end
