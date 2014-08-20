TARGET_CHIP := NRF51822_QFAA_CA
BOARD := BOARD_NRF6310
ASMFLAGS += -D__HEAP_SIZE=16 -D__STACK_SIZE=2048
CFLAGS += -DBLE_STACK_SUPPORT_REQD -DBOOTLOADER_BANKED -DBLE_STACK_SUPPORT_REQD -DS110 -DBOARD_NRF6310

DEVICESERIES := nrf51

C_SOURCE_FILES += main.c
C_SOURCE_FILES += dfu_dual_bank.c
C_SOURCE_FILES += dfu_transport_ble.c
C_SOURCE_FILES += bootloader.c
C_SOURCE_FILES += bootloader_util_gcc.c
C_SOURCE_FILES += $(SDK_PATH)Source/ble/ble_services/ble_dfu.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/app_timer.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/pstorage.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/hci_mem_pool.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/app_scheduler.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/app_gpiote.c
C_SOURCE_FILES += $(SDK_PATH)Source/app_common/crc16.c
C_SOURCE_FILES += $(SDK_PATH)Source/ble/ble_conn_params.c
C_SOURCE_FILES += $(SDK_PATH)Source/ble/ble_advdata.c
C_SOURCE_FILES += $(SDK_PATH)Source/ble/ble_services/ble_srv_common.c
C_SOURCE_FILES += $(SDK_PATH)Source/ble/softdevice_handler.c

INCLUDEPATHS += -I"$(SDK_PATH)Include/ble"
INCLUDEPATHS += -I"$(SDK_PATH)Include/app_common"
INCLUDEPATHS += -I"$(SDK_PATH)Include/s110"
INCLUDEPATHS += -I"$(SDK_PATH)Include/sd_common"
INCLUDEPATHS += -I"$(SDK_PATH)Include/ble/ble_services"
INCLUDEPATHS += -I"../include/ble_transport"
INCLUDEPATHS += -I"../include"
INCLUDEPATHS += -I"../"
SDK_PATH = ../../../../../

LINKER_SCRIPT = gcc_$(DEVICESERIES)_bootloader_$(DEVICE_VARIANT).ld
OUTPUT_FILENAME := $(OUTPUT_FILENAME)_bootloader_$(DEVICE_VARIANT)

DEVICE_VARIANT := xxaa
#DEVICE_VARIANT := xxab

USE_SOFTDEVICE := S110
#USE_SOFTDEVICE := S210

include $(SDK_PATH)Source/templates/gcc/Makefile.common
