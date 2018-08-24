ZEROClassic 1.0.14-1 -- WARNING! NOT RELEASED YET!
=======

What is ZEROClassic?
--------------

[ZEROClassic](https://github.com/LEAD-Anoy74/ZeroClassic/) is a fork of ZERO and Zcash.
Zcash is a fork of Bitcoin that adds shielded transaction via zk-SNARKs.

This software is the ZEROClassic node. It downloads and stores the entire history of ZEROClassic transactions, about 1GB at this point.
Depending on the speed of your computer and network connection, the synchronization process could take several hours.

**ZEROClassic is unfinished and highly experimental.** Use at your own risk.

Deprecation Policy
------------------
This release is considered deprecated 26 weeks after the release day. There
is an automatic deprecation shutdown feature which will halt the node some
time after this 26 week time period. The automatic feature is based on block
height and can be explicitly disabled.

Building
--------
Currently only Linux build is officially supported.  8GB RAM is recommended.

### Install packages (needs to be done only once)
```
sudo apt-get install \
      build-essential pkg-config libc6-dev m4 g++-multilib \
      autoconf libtool ncurses-dev unzip git python python-zmq \
      zlib1g-dev wget bsdmainutils automake cmake
```

### Download cryptographic keys (needs to be done only once)
```
./zcutil/fetch-params.sh
```

### Obtain the ZEROClassic software from GitHub
```
git clone https://github.com/LEAD-Anoy74/ZeroClassic
cd ZeroClassic
git checkout master
```

### Build the source code to produce binary executables:
```
./zcutil/build.sh --disable-rust -j$(nproc)
```
On a typical laptop -j3 works fine, while retaining some UI interactivity
```
./zcutil/build.sh --disable-rust -j3
```

