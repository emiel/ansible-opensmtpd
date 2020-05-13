Vagrant.configure("2") do |config|
  config.vm.box = "debian/buster64"
  config.vm.box_check_update = false

  config.vm.provider "virtualbox" do |v|
    v.cpus = 1
    v.memory = 1024
  end

  config.vm.provision "ansible" do |ansible|
    ansible.become = true
    ansible.compatibility_mode = "2.0"
    ansible.host_key_checking = false
    ansible.playbook = "tests/test.yml"
  end
end
