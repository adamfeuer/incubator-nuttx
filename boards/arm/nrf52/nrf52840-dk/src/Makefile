############################################################################
# boards/arm/nrf52/nrf52840-dk/src/Makefile
#
#   Copyright (C) 2019 Gregory Nutt. All rights reserved.
#   Author:  Mateusz Szafoni <raiden00@railab.me>
#
# Redistribution and use in source and binary forms, with or without
# modification, are permitted provided that the following conditions
# are met:
#
# 1. Redistributions of source code must retain the above copyright
#    notice, this list of conditions and the following disclaimer.
# 2. Redistributions in binary form must reproduce the above copyright
#    notice, this list of conditions and the following disclaimer in
#    the documentation and/or other materials provided with the
#    distribution.
# 3. Neither the name NuttX nor the names of its contributors may be
#    used to endorse or promote products derived from this software
#    without specific prior written permission.
#
# THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
# "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
# LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
# FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
# COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,
# INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
# BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS
# OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED
# AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
# LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
# ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
# POSSIBILITY OF SUCH DAMAGE.
#
############################################################################

include $(TOPDIR)/Make.defs

CSRCS = nrf52_boot.c nrf52_bringup.c

ifeq ($(CONFIG_LIB_BOARDCTL),y)
CSRCS += nrf52_appinit.c
endif

ifeq ($(CONFIG_ARCH_LEDS),y)
CSRCS += nrf52_autoleds.c
else
CSRCS += nrf52_userleds.c
endif

ifeq ($(CONFIG_ARCH_BUTTONS),y)
CSRCS += nrf52_buttons.c
endif

ifeq ($(CONFIG_NRF52_SPI_MASTER),y)
CSRCS += nrf52_spi.c
endif

ifeq ($(CONFIG_SENSORS_LSM6DSL),y)
CSRCS += nrf52_lsm6dsl.c
endif

ifeq ($(CONFIG_SENSORS_LSM303AGR),y)
CSRCS += nrf52_lsm303agr.c
endif

ifeq ($(CONFIG_SENSORS_HTS221),y)
CSRCS += nrf52_hts221.c
endif

ifeq ($(CONFIG_LPWAN_SX127X),y)
CSRCS += nrf52_sx127x.c
endif

ifeq ($(CONFIG_NRF52840DK_HIGHPRI),y)
CSRCS += nrf52_highpri.c
endif

ifeq ($(CONFIG_TIMER),y)
CSRCS += nrf52_timer.c
endif

include $(TOPDIR)/boards/Board.mk
