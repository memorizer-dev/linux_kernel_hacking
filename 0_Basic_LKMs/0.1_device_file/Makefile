obj-m += example.o
KDIR ?= /lib/modules/$(shell uname -r)/build

all:
	make -C $(KDIR) M=$(PWD) modules

clean:
	make -C $(KDIR) M=$(PWD) clean

test:
	sudo rmmod example
	sudo dmesg -C
	sudo insmod example.ko
	dmesg
