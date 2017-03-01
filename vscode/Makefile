all:
	set -x
	# Install dependencies
	cd app && ./scripts/npm.sh install
	# build vscode
	./node_modules/.bin/gulp "vscode-linux-ia32-prepare-flatpak"

install:
	./install

.PHONY: all install
