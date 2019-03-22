# MouseJacking
MouseJacking on Kali Linux with CrazyRadio PA.
My exploration of MouseJacking.

References:  
https://www.mousejack.com/  
https://github.com/insecurityofthings/jackit  
https://www.bettercap.org/modules/hid/  

## Sniffing Packets with Wireshark
First we need to setup the GNU Radio module and Wireshark dissector for the Nordic Semiconductor nRF24L Enhanced Shockburst protocol.

There are a few prerequisits we need to install first:
CMake
```
apt install cmake 
```

LibBoost  
```
apt install libboost-all-dev  
```

GnuRadio
```
apt install git cmake g++ libboost-all-dev libgmp-dev swig python3-numpy \
python3-mako python3-sphinx python3-lxml doxygen libfftw3-dev libcomedi-dev \
libsdl1.2-dev libgsl-dev libqwt-qt5-dev libqt5opengl5-dev python3-pyqt5 \
liblog4cpp5-dev libzmq3-dev
```
Git GnuRadio
```
git clone --recursive https://github.com/gnuradio/gnuradio
```
Build Gnuradio
```
cd gnuradio
mkdir build
cd build
cmake ../
make
```

Now we can clone the repository and build the 
```
git clone https://github.com/BastilleResearch/gr-nordic.git  
mkdir build
cd build
cmake ../
make
```

