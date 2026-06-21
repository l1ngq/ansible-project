# servers = [
#   {name: "web01", ip: "192.168.56.10", memory: "1048", cpu: "1"}
#   {name: "web02", ip: "192.168.56.10", memory: "1048", cpu: "1"}
#   {name: "lb01", ip: "192.168.56.10", memory: "2048", cpu: "1"}
#   {name: "db01", ip: "192.168.56.10", memory: "2048", cpu: "2"}
#   {name: "mon01", ip: "192.168.56.10", memory: "2048", cpu: "2"}
# ]
Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box = "ubuntu/jammy64"

  config.vm.define "web01" do |web01|
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "192.168.56.10"
    web01.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  config.vm.define "web02" do |web02|
    web02.vm.hostname = "web02"
    web02.vm.network "private_network", ip: "192.168.56.11"
    web02.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus = 1
    end
  end

  config.vm.define "lb01" do |lb01|
    lb01.vm.hostname = "lb01"
    lb01.vm.network "private_network", ip: "192.168.56.12"
    lb01.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

    config.vm.define "db01" do |db01|
    db01.vm.hostname = "db01"
    db01.vm.network "private_network", ip: "192.168.56.13"
    db01.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

  config.vm.define "mon01" do |mon01|
    mon01.vm.hostname = "mon01"
    mon01.vm.network "private_network", ip: "192.168.56.14"
    mon01.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 2
    end
  end

end
