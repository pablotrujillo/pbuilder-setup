# pbuilder-setup

basic:

sudo apt-get install pbuilder debootstrap devscripts --no-install-recommends

gedit $HOME/.pbuilderrc



create base.tar.gz, using panama mirror

sudo pbuilder --create --mirror "http://pa.archive.ubuntu.com/ubuntu"

update and install package in chroot (keep changes):

sudo pbuilder --login --safe-after-login 

make basic template package:
dh_make --createorig (-l -> library package, -s -> signle binary package, etc)

--creteorig -> create orig.ta.xz, used by  dpkg-buildpackage

builde on selfsystem:

dpkg-buildpackage -us -uc -rfakeroot

build usign pbuilder:

pdebuild --debbuildopts (-b -> binary package, -sa build source code and include it)

