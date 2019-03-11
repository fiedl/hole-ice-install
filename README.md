# Hole-Ice-Install

This repository provides reproducible install instructions for the hole-ice code and the icecube-simulation framework related to https://github.com/fiedl/hole-ice-study and https://github.com/fiedl/hole-ice-scripts.

## Installation on macOS

The file [install-on-mac-os-sierra.sh](install-on-mac-os-sierra.sh) contains instructions on how to install the IceCube-Simulation Framework with the hole-ice additions on macOS Sierra.

## Automated Build Using Vagrant

In order to have the install scriot run on a virtual machine, this repository provides [Vagrant](http://vagrantup.com) instructions in the [Vagrantfile](Vagrantfile).

```bash
# Clone this repository
git clone git@github.com:fiedl/hole-ice-install.git
```

For the automated code checkout to work, you need to provide svn credentials in a secrets file, which is not included in this repository. Please create the following file and provide credentials there:

```bash
# .secrets.sh
export SVN="our svn url"
export SVN_ICECUBE_USERNAME="our svn username"
export SVN_ICECUBE_PASSWORD="our svn password"
```

After that, install and run vagrant:

```bash
# Install Vagrant
brew cask instal vagrant

# Start the virtual machine and run the install instructions
vagrant up
```

After changing the install scripts, rerun via `vagrant provision` or `vagrant reload --provision`.

