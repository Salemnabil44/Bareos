deb http://archive.debian.org/debian/ stretch main
deb-src http://archive.debian.org/debian/ stretch main

sudo apt-get -o Acquire::Check-Valid-Until=false update
