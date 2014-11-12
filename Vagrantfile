# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/precise64"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.ssh.forward_agent = true

  config.vm.synced_folder "shared/", "/vagrant", id: "vagrant-root", :nfs => true


  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "provision/ansible/playbook.yml"
  end
end
