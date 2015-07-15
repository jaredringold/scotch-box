# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = true
  config.vm.define "scotch-box" do |node|
    node.vm.box = "scotch/box"
    node.vm.box_version < 2.0
    node.vm.hostname = "scotchbox"
    node.vm.network :private_network, ip: "192.168.33.10"
    node.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
    node.hostmanager.aliases = %w{www.scotchbox}
  end

end
