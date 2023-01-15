PROJ_ROOT := ..
ESP_ROOT := $(PROJ_ROOT)/makeEspArduino/esp32
CHIP := esp32
BUILD_DIR := build/$(CHIP)

ESPTOOL := $(ESP_ROOT)/tools/esptool/esptool.py

BUILD_EXTRA_FLAGS := -IGxEPD/src
BUILD_EXTRA_FLAGS += -IArduinoJson/src
BUILD_EXTRA_FLAGS += -IAsync/src
BUILD_EXTRA_FLAGS += -IESPAsyncWebServer/src
BUILD_EXTRA_FLAGS += -I$(PROJ_ROOT)/esp32/libraries/FS/src
BUILD_EXTRA_FLAGS += -I../libraries/Adafruit_GFX_Library
BUILD_EXTRA_FLAGS += -IAdafruit_BusIO
BUILD_EXTRA_FLAGS += -IAdafruit-GFX-Library
BUILD_EXTRA_FLAGS += -IAsyncTCP/src

SKETCH := weather_tiny.ino

ifneq ($(if $(V),$(V),0),0)
VERBOSE := 1
endif

include $(PROJ_ROOT)/makeEspArduino/makeEspArduino.mk

all: $(BUILD_DIR)/build_opt.h

$(BUILD_DIR)/build_opt.h: build_opt.h
	cp $< $@

#$(notdir $(SKETCH)).cpp: $(SKETCH) 
#	cp $< $@
