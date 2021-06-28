# antsdr-fw
[ANTSDR Firmware](https://github.com/MicroPhase/antsdr-fw) for the [ANTSDR](https://item.taobao.com/item.htm?spm=a230r.1.14.16.34e21142YIlxqx&id=647986963313&ns=1&abbucket=2#detail) .
This project is forked from ADI [ADALM-PLUTO ](https://github.com/analogdevicesinc/plutosdr-fw) ![ANTSDR](./images/ANTSDR.png)
## Build Instructions<br> 
The ANTSDR Firmware is built with the [Xilinx Vivado 2019.1](https://www.xilinx.com/member/forms/download/xef-vivado.html?filename=Xilinx_Vivado_SDK_Web_2019.1_0524_1430_Lin64.bin). You need to install the correct Vivado Version in your linux PC, and then, you can follow the instructions below to generate the firmware for [ANTSDR B220](https://item.taobao.com/item.htm?spm=a230r.1.14.16.34e21142YIlxqx&id=647986963313&ns=1&abbucket=2#detail).
```bash
sudo apt-get install git build-essential fakeroot libncurses5-dev libssl-dev ccache 
sudo apt-get install dfu-util u-boot-tools device-tree-compiler libssl1.0-dev mtools
sudo apt-get install bc python cpio zip unzip rsync file wget 
git clone --recursive https://github.com/MicroPhase/antsdr-fw.git 
cd ansdr-fw 
export CROSS_COMPILE=arm-linux-gnueabihf- 
export PATH=$PATH:/opt/Xilinx/SDK/2019.1/gnu/aarch32/lin/gcc-arm-linux-gnueabi/bin 
export VIVADO_SETTINGS=/opt/Xilinx/Vivado/2019.1/settings64.sh make
```
## Build Artifacts 
```bash 
wcc@wcc-dev:~/devel/ansdr-fw$ ls -AGhl build 
total 372M 
-rw-rw-r-- 1 wcc 69     4月14日 11:01 boot.bif 
-rw-rw-r-- 1 wcc 459K   4月14日 11:01 boot.bin 
-rw-rw-r-- 1 wcc 459K   4月14日 11:01 boot.dfu 
-rw-rw-r-- 1 wcc 588K   4月14日 11:01 boot.frm 
-rw-rw-r-- 1 wcc 254M   4月14日 11:01 legal-info-v0.33.tar.gz 
-rw-rw-r-- 1 wcc 527K   4月14日 11:03 LICENSE.html 
-rw-rw-r-- 1 wcc 11M    4月14日 11:01 ant.dfu 
-rw-rw-r-- 1 wcc 11M    4月14日 11:01 ant.frm 
-rw-rw-r-- 1 wcc 33     4月14日 11:01 ant.frm.md5 
-rw-rw-r-- 1 wcc 11M    4月14日 11:01 ant.itb 
-rw-rw-r-- 1 wcc 20M    4月14日 11:01 antsdr-fw-v0.33.zip 
-rw-rw-r-- 1 wcc 571K   4月14日 11:01 antsdr-jtag-bootstrap-v0.33.zip 
-rw-rw-r-- 1 wcc 442K   4月14日 11:00 ps7_init.c 
-rw-rw-r-- 1 wcc 442K   4月14日 11:00 ps7_init_gpl.c
-rw-rw-r-- 1 wcc 4,2K   4月14日 11:00 ps7_init_gpl.h 
-rw-rw-r-- 1 wcc 4,8K   4月14日 11:00 ps7_init.h
-rw-rw-r-- 1 wcc 2,4M   4月14日 11:00 ps7_init.html 
-rw-rw-r-- 1 wcc 31K    4月14日 11:00 ps7_init.tcl 
-rw-r--r-- 1 wcc 5,4M   4月14日 11:00 rootfs.cpio.gz 
drwxrwxr-x 6 wcc 4,0K   4月14日 11:01 sdk 
-rw-rw-r-- 1 wcc 52M    4月14日 11:03 sysroot-v0.33.tar.gz 
-rw-rw-r-- 1 wcc 943K   4月14日 11:01 system_top.bit 
-rw-rw-r-- 1 wcc 476K   4月14日 11:00 system_top.hdf 
-rwxrwxr-x 1 wcc 438K   4月14日 11:01 u-boot.elf 
-rw-rw---- 1 wcc 128K   4月14日 11:01 uboot-env.bin 
-rw-rw---- 1 wcc 129K   4月14日 11:01 uboot-env.dfu 
-rw-rw-r-- 1 wcc 6,5K   4月14日 11:01 uboot-env.txt 
-rwxrwxr-x 1 wcc 3,9M   4月14日 10:59 zImage 
-rw-rw-r-- 1 wcc 19K    4月14日 11:00 zynq-ant-sdr.dtb 
-rw-rw-r-- 1 wcc 19K    4月14日 11:00 zynq-ant-sdr-revb.dtb 
-rw-rw-r-- 1 wcc 19K    4月14日 11:00 zynq-ant-sdr-revc.dtb
 ```

