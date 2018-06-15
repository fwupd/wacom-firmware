# Copyright (C) 2017 Richard Hughes <richard@hughsie.com>

VENDOR=Wacom
PROJECT_NAME=Intuos_BT-M_BluetoothFW
VERSION=1.11
FIRMWARE_FILES=BluetoothFW_OakM_V1.11.airoflash
METAINFO_FILES=com.wacom.Intuos.BT-M.BluetoothFW.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
