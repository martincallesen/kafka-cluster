Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 8192
    v.cpus = 2
  end

  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 9021, host: 9021
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provisioning/docker_ubuntu1804/playbook.yml"
  end
end