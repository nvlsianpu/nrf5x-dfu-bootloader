# Prepare worksapce

You have to clone repositories into your project root (root of this repository): 
- BLE_API: 
    git clone https://github.com/ARMmbed/ble BLE_API
    cd BLE_API
    git checkout v2.1.1
- Mbed:
    git clone https://github.com/ARMmbed/mbed-os.git mbed
    cd mbed 
    git checkout mbed_lib_rev110
- nRF51822
    git clone https://github.com/ARMmbed/ble-nrf51822 nRF51822
    cd nRF51822
    git checkout v2.0.6


    Set the correct TOOLCHAIN_SYSROOT and HEX_TOOLS_ROOT pathes in CMakeLists.txt. 
    HEX_TOOLS_ROOT - it is a path to srecord tools for windows. This can be downloade from https://sourceforge.net/projects/srecord/files/srecord-win32/
    
# Build bootloader
Run cmake (makes sure that make is on you PATH):
    mkdir build
    cd build
    cmake –G “Unix Makefiles” ..
    make
