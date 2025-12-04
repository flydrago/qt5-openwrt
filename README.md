# qt5-openwrt

Qt 5.15.12 for OpenWrt 19.07 with Modbus & SerialPort support

## Features

- Qt 5.15.12 LTS version
- SerialPort module for serial communication
- SerialBus module for Modbus protocol support

## Available Packages

- qt5-core
- qt5-concurrent
- qt5-network
- qt5-widgets
- qt5-sql
- qt5-xml
- qt5-serialport
- qt5-serialbus
- qt5-xmlpatterns
- qt5-test

## Installation

1. Add feeds in `feeds.conf`:

```
src-git libqt https://github.com/Lankaster/qt5-openwrt.git
```

2. Update & install feeds:

```bash
./scripts/feeds update -a && ./scripts/feeds install -a
```

3. Select Qt5 packages in menuconfig:

```bash
make menuconfig
# Navigate to: Libraries -> Qt5
```

4. Build:

```bash
make package/qt5/compile V=s
```

## Dependencies

**Build Dependencies:**
- libiconv

**Runtime Dependencies:**
- librt
- zlib
- libstdcpp
- libpcre16
- libpthread
- libatomic

## Source Mirror

Qt source is downloaded from Aliyun mirror:
`https://mirrors.aliyun.com/qt/archive/qt/5.15/5.15.12/single/`
