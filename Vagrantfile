Vagrant.configure("2") do |config|
    config.vm.define "controlnode" do |controlnode|
      controlnode.vm.box = "ubuntu/focal64"
       controlnode.vm.hostname = "controlnode"
# change the interface name, from "enp8s0" to your
       controlnode.vm.network :public_network, bridge: "enp8s0"

    controlnode.vm.provision "ansible" do |ansible|
        ansible.galaxy_role_file = 'requirements.yml'
        ansible.playbook = "install_ansible.yml"
    end

    controlnode.vm.provider "virtualbox" do |vb|
         vb.memory = "4096"
         vb.cpus = 4
    end
end
end


