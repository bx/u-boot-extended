#
# (C) Copyright 2000-2003
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# SPDX-License-Identifier:	GPL-2.0+
#

obj-y	:= reset.o
obj-y	+= timer.o
obj-y	+= utils.o

ifneq ($(CONFIG_OMAP44XX)$(CONFIG_OMAP54XX),)
obj-y	+= hwinit-common.o
obj-y	+= clocks-common.o
obj-y	+= emif-common.o
obj-y	+= vc.o
obj-y	+= abb.o
endif

ifneq ($(CONFIG_OMAP54XX),)
obj-y	+= pipe3-phy.o
obj-$(CONFIG_SCSI_AHCI_PLAT) += sata.o
endif

ifeq ($(CONFIG_SYS_DCACHE_OFF),)
ifndef CONFIG_MIN_BOOT
obj-y	+= omap-cache.o
endif
endif

obj-y	+= boot-common.o
obj-y	+= lowlevel_init.o

obj-y	+= mem-common.o
