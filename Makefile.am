# Copyright 2018 SiFive, Inc
# SPDX-License-Identifier: Apache-2.0

bin_SCRIPTS = overlay-add

overlay-add: scripts/overlay-add
	ln -s $< $@
	chmod +x $@

EXTRA_DIST = scripts/overlay-add
EXTRA_DIST += README.md

clean-local:
	-rm -f overlay-add
