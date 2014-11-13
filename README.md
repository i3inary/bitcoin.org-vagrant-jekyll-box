## How to Setup a Local Dev Server for Bitcoin.org with a Vagrant Virtual Machine

This is intended to simply the process of setting up a Jekyll development environment and remove the barrier to entry required to contribute to bitcoin.org.

### Prerequisite Software Packages

Before going any further please make sure you have the most recent versions of the following:  

[Virtualbox](https://www.virtualbox.org/wiki/Downloads) *- allows you to create virtual machines on your local host machine*  
[Vagrant](https://www.vagrantup.com/) *- creates and configures virtualmachines from a universal configuration file*
  
### 1. Clone this Vagrant Virtual Machine Repository

First thing you will need is to grab the configuration files needed for vagrant to build a virtual machine automatically for you.  This will save you the trouble of getting you environment to work properly with the dependencies required to build the website files with Jekyll (the Ruby library used to generate the static website files).

    git clone https://github.com/i3inary/bitcoin.org-vagrant-jekyll-box
    cd bitcoin.org-vagrant-jekyll-box


### 2. Clone the Bitcoin.org Website Source Code

Now you will fork a fresh copy of the current [bitcoin.org repository](https://github.com/bitcoin/bitcoin.org.git) with your Github account and clone your new forked repository into the vagrant.  This step is outlined in detail 

*You should already be inside the bitcoin.org-vagrant-jekyll-box directory*

    git clone https://github.com/Airbitz/bitcoin.org.git bitcoin.org # this should be your forked version
    cd bitcoin.org
    git remote add upstream https://github.com/bitcoin/bitcoin.org.git


### 3. Automagically Build the Vagrant Machine

*You should already be inside the bitcoin.org-vagrant-jekyll-box directory*

    vagrant up
    cd /home/vagrant/bitcoin.org && bundle install

### 4. Start Your Jekyll Web Server

*You should already be inside the bitcoin.org-vagrant-jekyll-box directory*

    jekyll serve
    
## Additional Info

Misc tips and commands to make things go a little smoother.
