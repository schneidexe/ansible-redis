# This guide is optimized for Vagrant 1.7 and above.
# Although versions 1.6.x should behave very similarly, it is recommended
# to upgrade instead of disabling the requirement below.
Vagrant.require_version ">= 1.9.0"

Vagrant.configure("2") do |config|
  config.vm.define "redis1" do |redis1|
    redis1.vm.box = "ubuntu/xenial64"
    redis1.vm.hostname = "redis1"
    redis1.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: true
    redis1.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "playbook.yml"
    end
  end
  config.vm.define "redis2" do |redis2|
    redis2.vm.box = "ubuntu/xenial64"
    redis2.vm.hostname = "redis2"
    redis2.vm.network "private_network", ip: "192.168.50.11", virtualbox__intnet: true
    redis2.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "playbook.yml"
    end
  end
  config.vm.define "redis3" do |redis3|
    redis3.vm.box = "ubuntu/xenial64"
    redis3.vm.hostname = "redis3"
    redis3.vm.network "private_network", ip: "192.168.50.12", virtualbox__intnet: true
    redis3.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "playbook.yml"
    end
  end
end
