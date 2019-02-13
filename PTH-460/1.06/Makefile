# Copyright (C) 2016 Richard Hughes <richard@hughsie.com>

VENDOR=Wacom
PROJECT_NAME=IntuosPro
VERSION=1.06
FIRMWARE_FILES=	\
	viperS_v0106.wac	\
	AB1122_WACOM_ViperS_V1.00_IntuosProS_20181213.airoflash	\
	UPDATE_G11T_viper_0392_v0004_rev00.hex
METAINFO_FILES=	\
	PTH_460.metainfo.xml	\
	PTH_460_bluetooth.metainfo.xml	\
	PTH_460_touch.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
