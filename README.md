# TRex time-latency fork

This is a fork of the Cisco TRex [repo](https://github.com/cisco-system-traffic-generator/trex-core). 

I have added a way of saving latency and the timestamp of each packet captured by TRex. A .data file is created in the `scripts` folder. 

The regular README can be found [here](README_TREX.asciidoc).

## Build

Follow the regular build [guide](https://github.com/cisco-system-traffic-generator/trex-core/wiki#how-to-build-trex) or:

install clang-8 lldb-8 lld-8 clang-tools-8

```
cd linux_dpdk
CC=clang8  CXX=clang++-8 ./b configure
./b build
```

## Running 

There are some issues with ZMQ timeouts, so to run the server successfully you have to run it with the following options:

```bash
sudo ./t-rex-64 -i --hdrh --no-watchdog
```

