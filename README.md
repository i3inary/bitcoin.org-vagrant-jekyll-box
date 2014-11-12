## How to Setup a Local Dev Server for Bitcoin.org with a Vagrant Virtual Machine

This is intended to simply the process of setting up a Jekyll development environment and remove the barrier to entry required to contribute to bitcoin.org.


### Clone this Vagrant Virtual Machine Repository

This will grab the configuration files needed for vagrant to build a virtual machine automatically for you.  This will save you the trouble of getting you environment to work properly with the dependencies required to build the website files with Jekyll (the Ruby library used to generate the static website files).

    git clone https://github.com/i3inary/bitcoin.org-vagrant-jekyll-box
    cd bitcoin.org-vagrant-jekyll-box


### Clone the Bitcoin.org Website Source Code

Now fork a fresh copy of the current [bitcoin.org repository](https://github.com/bitcoin/bitcoin.org.git) with your Github account and clone your new forked repository into the vagrant.

*You should already be inside the **bitcoin.org-vagrant-jekyll-box** directory*

    git clone https://github.com/Airbitz/bitcoin.org.git bitcoin.org # this should be your forked version
    cd bitcoin.org
    git remote add upstream https://github.com/bitcoin/bitcoin.org.git


### Build the Vagrant Machine

This step requires that you have [Vagrant](https://www.vagrantup.com/) installed.  

*You should already be inside the **bitcoin.org-vagrant-jekyll-box** directory*

    vagrant up
