# Copyright 2018 SiFive, Inc
# SPDX-License-Identifier: Apache-2.0

bin_SCRIPTS = fsdk-add-overlay fsdk-generate-overlay fsdk-create-project

fsdk-add-overlay: scripts/overlay-add
	cat $< | sed 's:EPREFIX:@EPREFIX@:g' | sed 's:TMP1TAG:@EPREFIX@:g' | sed 's:TMP2TAG:EPREFIX:g' > $@
	chmod +x $@

fsdk-generate-overlay: scripts/overlay-generator
	cat $< > $@
	chmod +x $@

fsdk-create-project: scripts/create-project
	cat $< | sed 's:EPREFIX:@EPREFIX@:g' > $@
	chmod +x $@

EXTRA_DIST = scripts/overlay-add
EXTRA_DIST += scripts/overlay-generator
EXTRA_DIST += scripts/create-project
EXTRA_DIST += README.md

clean-local:
	-rm -f fsdk-add-overlay
	-rm -f fsdk-generate-overlay
	-rm -f fsdk-create-project
