all:
	set -x
	# Install dependencies
	cd app && ./scripts/npm.sh install && ./scripts/npm.sh install gm
	# build vscode
	cd app && ./node_modules/.bin/gulp "vscode-linux-ia32-prepare-flatpak" --max_old_space_size=4096;

install:
	./install

.PHONY: all install
