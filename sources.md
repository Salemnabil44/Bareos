deb http://archive.debian.org/debian/ stretch main
deb-src http://archive.debian.org/debian/ stretch main

sudo apt-get -o Acquire::Check-Valid-Until=false update

wget -q -O - http://download.bareos.org/bareos/release/latest/Ubuntu_22.04/Release.key | sudo gpg --dearmor -o /usr/share/keyrings/bareos-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/bareos-archive-keyring.gpg] http://download.bareos.org/bareos/release/latest/Ubuntu_22.04/ /" | sudo tee /etc/apt/sources.list.d/bareos.list
sudo apt update
