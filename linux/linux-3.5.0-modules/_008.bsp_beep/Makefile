obj-m += beep_module.o

KERNEL = /home/user/Workspace/exynos/kernel
SHARE = /home/user/Share

all:
	make -C $(KERNEL) M=`pwd` modules
	arm-linux-gcc beep_app.c -o app
	rm -rf $(SHARE)/*
	cp -f *.ko $(SHARE)/
	cp -f app $(SHARE)/
	make clean
	@echo "\033[31m >>>>>> make all successful <<<<<< \033[0m"
clean:
	make -C $(KERNEL) M=`pwd` modules clean
	rm -f app
