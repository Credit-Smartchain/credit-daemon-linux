Install the required dependencies.

sudo apt-get install build-essential libdb-dev libdb++-dev libboost-all-dev git libssl1.0-dev

sudo apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev

Create a directory for the source code.

mkdir source_code

cd source_code

Download the source code

wget "https://terra-credit.com/credit-daemon-linux.tar.gz" -O credit-source.tar.gz

Extract the tar file.

tar -xzvf credit-source.tar.gz

Go to the src directory of your source code.

cd src

Execute the following command to compile the daemon.

make -f makefile.unix RELEASE=1
