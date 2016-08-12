Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/precise64"

  config.vm.network :private_network, ip: "192.168.42.33"

  config.vm.provider :virtualbox do |v|
    v.customize ["modifyvm", :id, "--memory", 1024]
  end

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.module_path = "modules"
    puppet.options = ['--verbose']
  end
end
