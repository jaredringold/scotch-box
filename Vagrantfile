# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "scotch/box"

  # setup virtual hostname and provision local IP
  config.vm.hostname = "scotchbox"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.hostsupdater.aliases = %w{www.scotchbox}
  config.hostsupdater.remove_on_suspend = true

  config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]

end
