# Copyright (C) 2019 Logitech

VENDOR=Logitech
PROJECT_NAME=K850
VERSION=MPK04.02_B0014
FIRMWARE_FILES=../MPK04.02_B0014.dfu
METAINFO_FILES=com.logitech.MPK04.metainfo.xml

all: $(VENDOR)-$(PROJECT_NAME)-$(VERSION).cab

clean:
	rm -f *.cab

check: $(METAINFO_FILES)
	appstream-util validate-relax $(METAINFO_FILES)

%.cab: $(FIRMWARE_FILES) $(METAINFO_FILES)
	gcab --create --nopath $@ $(FIRMWARE_FILES) $(METAINFO_FILES)
