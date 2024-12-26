apt remove --auto-remove yersinia
apt purge --auto-remove yersinia

git clone https://github.com/infosecconsultant/yersinia.git
cd yersinia/
sudo apt update && sudo apt upgrade && sudo apt install autoconf automake autotools-dev libnet1-dev libgtk2.0-dev libpcap-dev
./autogen.sh
./configure
make
sudo make install

yersinia -G