Vagrant.configure("2") do |config|

  config.vm.box = "Official Ubuntu 14.04 daily Cloud Image amd64 (Development release, No Guest Additions)"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box"
  config.vm.network :forwarded_port, host: 4000, guest: 4000

  config.vm.provision :shell,
    :inline => "sudo apt-get update && sudo apt-get -y install curl language-pack-en"
  config.vm.provision :shell, :path => "install-rvm.sh",  :args => "stable"
  config.vm.provision :shell, :path => "install-ruby.sh", :args => "2.0.0 bundler"

  config.vm.synced_folder "./bitcoin.org", "/home/vagrant/bitcoin.org", :create => true


  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--cpuexecutioncap", "100"]
    v.memory = 1024
    v.cpus = 2
  end


end

