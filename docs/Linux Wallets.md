Linux  Building
===============
Built on Ubuntu 14.04 (Trusty)
### DAEMON
Update dependancy repository:
```
apt-get update
```
Install dependancies:
```
apt-get install git nano libminiupnpc-dev libqrencode-dev build-essential libssl-dev libboost-all-dev libdb++-dev
```
Download HOST source from github:
```
git clone https://github.com/Ace-Of-Fades/HOST.git
```	
Move to the HOST src directory:
```
cd HOST/src
```
Edit file permissions for "leveldb" folder:
```
chmod -R 775 leveldb
```
Build the daemon:
```
make -f makefile.unix
```

In the src directory, search for "HOSTd". **You now have your daemon wallet!** If you would like to add the enviroment variable for quick and easy control of the wallet, continue to the step below. It's however, completely optional. 

Open your ./profile file:
```
nano ~/.profile
```
(Add the following line to the bottom of the document, then save it.)
```
export PATH="$PATH:<Your HOSTd Location Directory>"
```
Now logout:
```
logout
```
When you log back in, you will be able to start the daemon by simply typing:
```
HOSTd
```
### QT
Update dependancy repository:
```
apt-get update
```
Install dependancies:
```
apt-get install git nano qt4-qmake libqt4-dev libminiupnpc-dev libqrencode-dev build-essential libssl-dev libboost-all-dev libdb++-dev
```
Download HOST source from github:
```
git clone https://github.com/Ace-Of-Fades/HOST.git
```	
Move to the HOST directory:
```
cd HOST
```
Edit file permissions for "leveldb" folder:
```
chmod -R 775 src/leveldb
```
Build the daemon:
```
qmake && make
```

In the HOST directory, search for "HOST-qt". **You now have your QT wallet!**