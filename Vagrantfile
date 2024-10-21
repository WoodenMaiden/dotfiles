# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    # Define the number of virtual machines you want to create
    num_vms = unless ENV['NUM_VM'].nil? then ENV['NUM_VM'].to_i else 4 end
  
    # Define a list of predefined hostnames
    predefined_hostnames = ["Excalibur", "Mag", "Volt", "Trinity"]
  
    # Loop to create each virtual machine
    (1..num_vms).each do |i|
      config.vm.define "vm#{i}" do |node|
        node.vm.box = "generic/debian11" # Specify the base box
        node.vm.hostname = predefined_hostnames[i - 1] # Assign predefined hostname
        node.vm.network "private_network", ip: "192.168.50.#{i + 10}" # Set private IP
        node.vm.provider "libvirt" do |libvirt|
          libvirt.driver = "kvm" # Set KVM as the driver
          libvirt.memory = 512 # Set memory size for the VM
          libvirt.cpus = 1 # Set number of CPUs for the VM
        end
      end
    end
  end
  
