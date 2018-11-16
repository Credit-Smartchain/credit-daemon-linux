You can setup a node on Ubuntu server using the following instructions.

Rent a VPS running Ubuntu 18.04 server.

Update your VPS using the following commands.

sudo apt-get update
sudo apt-get upgrade

Install the necessary dependencies using the following commands.

sudo apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0-dev
sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

Download the daemon file from github https://github.com/Terra-Credit-Union/credit-daemon-linux

Extract the tar file using the following command.

tar -xzvf credit-daemon-linux.tar.gz

Install the daemon.

chmod +x creditd
sudo mv creditd /usr/bin/

Create the config file.

mkdir $HOME/.credit
nano $HOME/.credit/credit.conf

Paste the following lines in credit.conf.

rpcuser=your_username
rpcpassword=your_password
rpcallowip=127.0.0.1
listen=1
server=1
txindex=1
daemon=1

Start your node with the following command.

creditd
