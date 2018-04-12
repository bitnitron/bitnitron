bitnitron integration/staging tree
================================

https://bitnitron.com

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Bitnitron Developers

What is Bitnitron?
----------------

Bitnitron is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2016 blocks to retarget difficulty

For more information, as well as an immediate usability, binary version of the Bitnitron client software, see https://bitnitron.com.

License
-------

Bitnitron is released under the terms of the MIT license. See `COPYING` for more information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Bitnitron development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't match the project's coding conventions (see `doc/coding.txt`) or are controversial.


Testing
-------

Testing and code review is the bottleneck for development; we get more pull requests than we can review and test. Please be patient and help out, and remember this is a security-critical project where any mistake might cost people lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./bitnitron-qt_test


### General Information

Coin Site : https://bitnitron.com

Block Explorer : https://btnexplorer.com

COIN INFO :-

Algorithm : Scrypt

Type : PoW

Coin name : bitnitron

Coin abbreviation : BTN

Address letter : B

RPC port : 35948

P2P port : 35947

Block reward : 1000 coins

Block halving : 475000 blocks

Coin supply : 1000000000 coins

Premine amount : 50000000 coins

Coinbase maturity : 10 blocks

Target spacing : 2 minutes

Target timespan : 5 minutes

Transaction confirmations : 2 blocks



 
Installation
===========================

The installation requires at least a VPS having 2 GB OF RAM, 2 CORE CPU AND 40GB HDD with UBUNTU 16.04 installed on it. 

Steps:
 
1) Update your Ubuntu 16.04 machine.

sudo apt-get update

sudo apt-get upgrade

2) Install the dependencies to compile from source code.

sudo apt-get install build-essential libssl-dev libdb++-dev git libssl1.0.0-dbg libdb-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev 

3) Download source code from repository.

git clone https://github.com/bitnitron/bitnitron.git

4) Go to the src directory of your coin.

cd bitnitron/src

5)  Now Run the following commands

chmod +x leveldb/build_detect_platform

6) Execute the following command to compile the daemon.

make -f makefile.unix RELEASE=1

7) Run the Coin Server using ./bitnitrond command

You will see message to create username and password

8) Create a new configuration file.

sudo nano /root/.bitnitron/bitnitron.conf

9) Paste the following lines in bitnitron.conf file and save it.

rpcuser=rpc_bitnitron

rpcpassword=yourrandompassword

rpcallowip=127.0.0.1

listen=1

server=1

txindex=1

daemon=1

10) Run the Coin Server using ./bitnitrond command


List of API call list can be found here : https://en.bitcoin.it/wiki/Original_Bitcoin_client/API_calls_list



Cheers...
