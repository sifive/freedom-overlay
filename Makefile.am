# Copyright 2018 SiFive, Inc
# SPDX-License-Identifier: Apache-2.0

bin_SCRIPTS = overlay-add

overlay-add: scripts/overlay-add
	cat $< | sed 's:PREFIX:@PREFIX@:g' | sed 's:TMP1TAG:@PREFIX@:g' | sed 's:TMP2TAG:PREFIX:g' > $@
	chmod +x $@

EXTRA_DIST = scripts/overlay-add
EXTRA_DIST += README.md

clean-local:
	-rm -f overlay-add
