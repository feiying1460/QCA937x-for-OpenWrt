#
# Makefile fragment for Broadcom 802.11n Networking Device Driver
#
# Copyright (c) 2010 Broadcom Corporation
#
# Permission to use, copy, modify, and/or distribute this software for any
# purpose with or without fee is hereby granted, provided that the above
# copyright notice and this permission notice appear in all copies.
#
# THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
# WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
# MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY
# SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
# WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION
# OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN
# CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

ccflags-y += \
	-I$(backport_srctree)/drivers/net/wireless/brcm80211/brcmfmac	\
	-I$(backport_srctree)/drivers/net/wireless/brcm80211/include

ccflags-y += -D__CHECK_ENDIAN__

obj-$(CPTCFG_BRCMFMAC) += brcmfmac.o
brcmfmac-objs += \
		wl_cfg80211.o \
		fwil.o \
		fweh.o \
		fwsignal.o \
		p2p.o \
		proto.o \
		bcdc.o \
		dhd_common.o \
		dhd_linux.o \
		nvram.o \
		btcoex.o
brcmfmac-$(CPTCFG_BRCMFMAC_SDIO) += \
		dhd_sdio.o \
		bcmsdh.o \
		sdio_chip.o
brcmfmac-$(CPTCFG_BRCMFMAC_USB) += \
		usb.o
brcmfmac-$(CPTCFG_BRCMDBG) += \
		dhd_dbg.o
brcmfmac-$(CPTCFG_BRCM_TRACING) += \
		tracepoint.o
