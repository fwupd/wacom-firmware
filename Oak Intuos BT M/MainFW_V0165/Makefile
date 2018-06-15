# Copyright (C) 2017 Richard Hughes <richard@hughsie.com>

VENDOR=Wacom
PROJECT_NAME=Intuos_BT-M_MainFW
VERSION=1.65
FIRMWARE_FILES=MainFW_OakM_Ver0165.wac
METAINFO_FILES=com.wacom.Intuos.BT-M.MainFW.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
