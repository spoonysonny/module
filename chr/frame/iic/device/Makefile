# Makefile2.6

ifneq ($(KERNELRELEASE),)
	# kbuild syntax. dependency relationshsip of files and target modules are listed here.
	# mymodule-objs := chr_iic_dev.o
	# mymodule-objs := i2c_boardinfo.o
	obj-m := chr_iic_dev.o
else
	PWD  := $(shell pwd)
	KDIR := ~/project/git/rpi_linux

all:
	$(MAKE) -C $(KDIR) M=$(PWD) modules ARCH=arm  CROSS_COMPILE=arm-bcm2708-linux-gnueabi-
clean:
	rm -rf .*.cmd *.o *.mod.c *.ko .tmp_versions *.order *.symvers

endif
