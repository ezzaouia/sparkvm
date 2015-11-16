# -*- mode: ruby -*-
# vi: set ft=ruby :

ipythonPort = 8001


Vagrant.configure(2) do |config|
  
#  config.ssh.insert_key = true

  config.vm.define "sparkvm" do |master|
  
    # Create a forwarded port mapping which allows access to a specific port
    # within the machine from a port on the host machine. In the example below,
    # accessing "localhost:8080" will access port 80 on the guest machine.
    master.vm.network "forwarded_port", guest: 8888, host: 8888, auto_correct: true
    
    # Every Vagrant development environment requires a box. You can search for
    # boxes at https://atlas.hashicorp.com/search.
    master.vm.box = "https://cloud-images.ubuntu.com/vagrant/wily/current/wily-server-cloudimg-amd64-vagrant-disk1.box"
    
#    master.vm.synced_folder "/Users/ror/Workspace/code/sparkvm/notebook",
    
    master.vm.box_check_update = true

     master.vm.provider "virtualbox" do |vb|
       # Display the VirtualBox GUI when booting the machine
       # vb.gui = true
       vb.name = 'sparkvm'

       # Customize the amount of memory on the VM:
       vb.memory = "4096"
     end

  end
  
end
