
#Delete obj file first

#OBJFILE=$(objtree)/fs/proc/info/config_info.o
#$(shell rm $(OBJFILE) -f)


#FORCE will make sure this obj be compiled every time
ifneq ($(KERNELRELEASE),)
obj-m += ram.o
else
PWD = $(shell pwd)
K_DIR = ${PWD}/../../../kernel_obj
all:
#	make -C $(K_DIR) M=$(PWD) modules ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu-
	make -C $(K_DIR) M=$(PWD) modules ARCH=arm CROSS_COMPILE=arm-linux-gnueabi-
clean:
	make -C $(K_DIR) M=$(PWD) clean
endif
