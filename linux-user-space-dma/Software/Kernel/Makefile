EXTRA_CFLAGS := -I$(src)/../Common

ifneq ($(KERNELRELEASE),)

obj-m := dma-proxy.o

else

all:	modules

clean:
	$(MAKE) -C $(KDIR) M=$(PWD) clean

modules:
	$(MAKE) -C $(KDIR) M=$(PWD) modules

modules_install:	modules
	$(MAKE) -C $(KDIR) M=$(PWD) modules_install

endif
