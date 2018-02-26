# SukaCoin

SukaCoin is a PoW + PoS-based cryptocurrency.

SukaCoin uses libsecp256k1,
			  libgmp,
			  Boost1.55,
			  OR Boost1.57,  
			  Openssl1.01m,
			  Berkeley DB 4.8,
			  QT5 to compile


Block Spacing: 120 Seconds
Stake Minimum Age: 8 Hours

Port: 48744
RPC Port: 48844


BUILD LINUX (see the [Wiki](https://github.com/AShelter/DemoCoin/wiki/Unix-Build) for dependencies)
-----------
1) git clone https://github.com/AShelter/DemoCoin

2) cd DemoCoin/src

3) mkdir obj/crypto

4) chmod +x leveldb/build_detect_platform

5) cd leveldb && make libleveldb.a libmemenv.a

6) cd ..

7) sudo make -f makefile.unix USE_UPNP=    # Headless SukaCoin

8) strip sukacoind

9) sudo cp sukacoind /usr/local/bin





BUILD WINDOWS
-------------

1) Download Qt.zip from https://github.com/AShelter/DemoCoin/releases/tag/v1.0 and unpack to C:/

2) Download SukaCoin source from https://github.com/AShelter/DemoCoin/archive/master.zip 

2.1) Unpack to C:/DemoCoin

3) Install Perl for windows from the homepage http://www.activestate.com/activeperl/downloads

4) Download Python 2.7 https://www.python.org/downloads/windows/

4.1) While installing python make sure to add python.exe to the path.

5) Run msys.bat located in C:\MinGW49-32\msys\1.0

6) cd /C/SukaCoin/src/leveldb

7) Type "TARGET_OS=NATIVE_WINDOWS make libleveldb.a libmemenv.a" and hit enter to build leveldb

8) Exit msys shell

9) Open windows command prompt

10) cd C:/dev

11) Type "49-32-qt5.bat" and hit enter to run

12) cd ../SukaCoin

13) Type "qmake USE_UPNP=0" and hit enter to run

14) Type "mingw32-make" and hit enter to start building. When it's finished you can find your .exe in the release folder.
