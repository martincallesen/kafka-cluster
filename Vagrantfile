Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 8192
    v.cpus = 2
  end

  config.vm.box = "ubuntu/bionic64"
  # Kafka Control Center
  config.vm.network "forwarded_port", guest: 9021, host: 9021
  # Kafka Broker
  config.vm.network "forwarded_port", guest: 9092, host: 9092
  # Kafka ksql-server
  config.vm.network "forwarded_port", guest: 8088, host: 8088
  # Kafka connect
  config.vm.network "forwarded_port", guest: 8083, host: 8083
 # Kafka rest-proxy
  config.vm.network "forwarded_port", guest: 8082, host: 8082
 # Kafka rest-proxy
  config.vm.network "forwarded_port", guest: 8082, host: 8082

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end
end