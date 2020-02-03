Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provisioning/docker_ubuntu1804/playbook.yml"
  end
end