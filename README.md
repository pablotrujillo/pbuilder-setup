# pbuilder-setup

basic:

sudo apt-get install pbuilder debootstrap devscripts --no-install-recommends

gedit $HOME/.pbuilderrc



create base.tar.gz, using panama mirror:
sudo pbuilder --create --mirror "http://pa.archive.ubuntu.com/ubuntu"



