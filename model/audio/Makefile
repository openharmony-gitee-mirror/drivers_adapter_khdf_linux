#
# Copyright (c) 2021 Huawei Device Co., Ltd.
#
# This software is licensed under the terms of the GNU General Public
# License version 2, as published by the Free Software Foundation, and
# may be copied, distributed, and modified under those terms.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
#

KHDF_AUDIO_BASE_ROOT_DIR = ../../../../../..
KHDF_AUDIO_KHDF_ROOT_DIR = drivers/hdf/khdf
KHDF_FRAMEWORK_ROOT_DIR = drivers/hdf/framework
KHDF_AUDIO_ROOT_DIR = ../../../../../framework/model/audio
KHDF_AUDIO_HI3516DV300_DIR = $(KHDF_AUDIO_BASE_ROOT_DIR)/drivers/peripheral/audio/chipsets/hi3516dv300
KHDF_AUDIO_HI3516DV300_INC_DIR = drivers/hdf/framework/../peripheral/audio/chipsets/hi3516dv300

obj-$(CONFIG_DRIVERS_HDF_AUDIO) += \
          $(KHDF_AUDIO_ROOT_DIR)/core/src/audio_core.o \
          $(KHDF_AUDIO_ROOT_DIR)/core/src/audio_host.o \
          $(KHDF_AUDIO_ROOT_DIR)/core/src/audio_parse.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_accessory_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_codec_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_dsp_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_dai_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_platform_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/common/src/audio_dma_base.o \
          $(KHDF_AUDIO_ROOT_DIR)/sapm/src/audio_sapm.o \
          $(KHDF_AUDIO_ROOT_DIR)/dispatch/src/audio_stream_dispatch.o \
          $(KHDF_AUDIO_ROOT_DIR)/dispatch/src/audio_control_dispatch.o

obj-$(CONFIG_DRIVERS_HDF_AUDIO_HI3516CODEC) += \
          $(KHDF_AUDIO_HI3516DV300_DIR)/../tfa9879/accessory/src/tfa9879_accessory_adapter.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/../tfa9879/accessory/src/tfa9879_accessory_impl.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/codec/src/hi3516_codec_adapter.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/codec/src/hi3516_codec_impl.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/codec/src/hi3516_codec_ops.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/dsp/src/dsp_adapter.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/dsp/src/dsp_ops.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/soc/src/hi3516_dai_adapter.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/soc/src/hi3516_dai_ops.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/soc/src/hi3516_aiao_impl.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/soc/src/hi3516_dma_ops.o \
          $(KHDF_AUDIO_HI3516DV300_DIR)/soc/src/hi3516_dma_adapter.o

ccflags-$(CONFIG_DRIVERS_HDF_AUDIO) += -lm -lc -lgcc -std=gnu99 -Werror \
             -I$(srctree)/$(KHDF_AUDIO_KHDF_ROOT_DIR)/osal/include \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/core \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/utils \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/osal \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/platform \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/config \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/include/audio \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/ability/sbuf/include \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/core/common/include/host \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/model/audio/core/include \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/model/audio/sapm/include \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/model/audio/dispatch/include \
             -I$(srctree)/$(KHDF_FRAMEWORK_ROOT_DIR)/model/audio/common/include \
             -I$(srctree)/bounds_checking_function/include

ccflags-$(CONFIG_DRIVERS_HDF_AUDIO_HI3516CODEC) += \
             -I$(srctree)/$(KHDF_AUDIO_HI3516DV300_INC_DIR)/codec/include \
             -I$(srctree)/$(KHDF_AUDIO_HI3516DV300_INC_DIR)/soc/include \
             -I$(srctree)/$(KHDF_AUDIO_HI3516DV300_INC_DIR)/dsp/include \
             -I$(srctree)/$(KHDF_AUDIO_HI3516DV300_INC_DIR)/../tfa9879/accessory/include
