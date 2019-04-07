Use the following instructions to setup a node on Ubuntu Server 18.04.

Install Ubuntu Server 18.04 on a VPS.

Update your Ubuntu machine.

sudo apt-get update
sudo apt-get upgrade

Install the required dependencies.

sudo apt-get install build-essential libdb-dev libdb++-dev libboost-all-dev git libssl1.0-dev
sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

Download the source code

wget "https://terra-credit.com/credit-daemon-linux.tar.gz" -O credit-daemon-linux.tar.gz

Extract the tar file.

tar -xzvf credit-daemon-linux.tar.gz

Install the daemon.

chmod +x creditd
sudo mv creditd /usr/bin/

Create the config file.

mkdir $HOME/.credit
nano $HOME/.credit/credit.conf

Paste the following lines in credit.conf.

rpcuser=rpc_credit (example)

rpcpassword=69c863e3356d3dae95df454a1 (Example)

rpcallowip=127.0.0.1

listen=1

server=1

txindex=1

daemon=1


Start your node with the following command.

creditd
