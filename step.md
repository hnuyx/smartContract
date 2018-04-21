
smart contract development

1. install etherenum and go-ethereum
epel: the third source package
ntp: time sync

tools: epel-release, ntp, git, wget, bzip2, vim, gcc-c++, nodejs, cmake
## yum install epel-release
## yum install ntp

2. install golang 1.9
# wget https://storage.googleapis.com/golang/go1.9.linux-amd64.tar.gz
# tar xzvf go1.9.linux-amd64.tar.gz
# mv go /usr/local/
configure GOROOT and PATH
# echo "export GOROOT=/usr/local/go" >> /etc/profile
# echo "export PATH=$PATH:/usr/local/go/bin/" >> /etc/profile
# source /etc/profile

3. clone go-ethereum
# git clone https://github.com/ethereum/go-ethereum.git 
# cd go-ethereum
# make geth
or
# make all

#############################Please ignore this block 4-6##########################################
4. all install below as pre-environment
# yum install repolist
# yum install dpkg
# yum install dpkg-dev
# yum install dpkg-devel
# yum install curl curl-devel libtool libtool-ltdl libtool-ldtl-devel

5. pip tool
# yum install python
# curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
# python get-pip.py
# pip install --upgrade pip
# pip install bitcoin
# pip install leveldb
# pip install plyvel

6. faild insstall pyton-pysha3

###################################################################################################

7. install cmake 3.0+
download from https://cmake.org/download/
# wget https://cmake.org/files/v3.11/cmake-3.11.1.tar.gz
# tar xzvf cmake-3.11.1.tar.gz
# ./bootstrap && make
# make install

8. start ntpd
# systemctl enable ntpd
# systemctl start ntpd

9. star firewall and allow port 8078 and 30303
# yum install firewalld
# systemctl start firewalld
# firewall-cmd --zone=public --add-port=8087/tcp --permanent
# firewall-cmd --zone=public --add-port=30303/tcp --permanent

10. configure genesis.json
11. options
--nodiscover
--maxpeers 0
--rpc
--rpcapi "db, eth, net, web3"
--rpcport "8080"
--rpccorsdomain "http://xxxxxxxx/"
--datadir "/home/TestChain"
--identity "TestnetMainNode"

ex:
# geth --datadir "/home/henry/myEtherum/ebase/chain"  --nodiscover console 2>> geth.log

12. geth command
> eth.accounts
> personal.newAccount()
> eth.getBalance(eth.accounts[0])
> minner.start()
> minner.stop()
