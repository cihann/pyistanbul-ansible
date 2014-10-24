# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "pyistanbul"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.network :private_network, ip: "192.168.33.20"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant.yml"
    ansible.host_key_checking = false
    ansible.verbose = "v"
  end
end
