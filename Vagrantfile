Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.cpus= 2
  end

  config.vm.network "private_network", type: "dhcp"

  config.vm.define "node1" do |node1|
    node1.vm.hostname = 'node1'
#    node1.vm.network :private_network, ip: "192.168.10.101"
  end

#   config.vm.define "node2" do |node2|
#     node2.vm.hostname = 'node2'
# #    node2.vm.network :private_network, ip: ""
#   end

  config.ssh.insert_key=false

  config.vm.provision "ansible" do |ansible|
    ansible.verbose="v"
    ansible.playbook="playbook.yml"
  end

end
