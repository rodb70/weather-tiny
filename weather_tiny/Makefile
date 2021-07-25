PROJ_ROOT := /home/rod/workspace/esp32
ESP_ROOT := $(PROJ_ROOT)/esp32
CHIP := esp32

BUILD_EXTRA_FLAGS := -IGxEPD/src
BUILD_EXTRA_FLAGS += -IArduinoJson/src
BUILD_EXTRA_FLAGS += -IAsync/src
BUILD_EXTRA_FLAGS += -IESPAsyncWebServer/src
BUILD_EXTRA_FLAGS += -I$(PROJ_ROOT)/esp32/libraries/FS/src
BUILD_EXTRA_FLAGS += -I../libraries/Adafruit_GFX_Library
BUILD_EXTRA_FLAGS += -D_font_h

ifneq ($(if $(V),$(V),0),0)
VERBOSE := 1
endif

include $(PROJ_ROOT)/makeEspArduino/makeEspArduino.mk
