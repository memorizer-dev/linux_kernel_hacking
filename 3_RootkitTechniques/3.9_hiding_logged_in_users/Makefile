obj-m += rootkit.o
KDIR ?= /lib/modules/$(shell uname -r)/build

all:
	make -C $(KDIR) M=$(PWD) modules
	gcc -o enum_utmp enum_utmp.c

clean:
	make -C $(KDIR) M=$(PWD) clean
	rm enum_utmp
