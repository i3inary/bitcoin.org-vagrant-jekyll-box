Vagrant.configure("2") do |config|

  config.vm.box = "precise32"
  config.vm.box_url = "http://files.vagrantup.com/precise32.box"
  config.vm.network :forwarded_port, host: 4000, guest: 4000
  config.vm.provision :shell,
    :inline => "sudo apt-get update && sudo apt-get -y install build-essential git python-software-properties &&  sudo apt-add-repository -y ppa:brightbox/ruby-ng && sudo apt-get update && sudo apt-get -y install ruby2.0 ruby2.0-dev libicu48 && gem install bundler && cd /home/vagrant/bitcoin.org && bundle install && cd /home/vagrant/bitcoin.org/_site && bundle exec jekyll build"

  config.vm.synced_folder "../bitcoin.org", "/home/vagrant/bitcoin.org", :create => true
end

