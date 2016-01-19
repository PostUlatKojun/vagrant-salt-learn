Vagrant.configure("2") do |config|
  ## Choose your base box
  config.vm.box = "precise64"

  ## For masterless, mount your salt file root
  config.vm.synced_folder "salt/roots/", "/srv/salt/"

  config.vm.hostname = "dev-my-app"
  config.vm.network :private_network, ip: '3.3.3.3'

  ## Use all the defaults:
  config.vm.provision :salt do |salt|

    salt.minion_config = "salt/minion.yml"
    salt.run_highstate = true

  end
end

