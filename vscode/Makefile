all:
	set -x
	# Install dependencies
	cd app && ./scripts/npm.sh install && ./scripts/npm.sh install gm
	# build vscode
	cd app && ./node_modules/.bin/gulp "vscode-linux-ia32-prepare-flatpak" --max_old_space_size=4096;

install:
	# Install Icons, appdata.xml and .desktop file
	mkdir -p /export/share/
	cp -r app/.build/linux/flatpak/i386/share/icons /export/
	cp -r app/.build/linux/flatpak/i386/share/appdata /export/
	cp -r app/.build/linux/flatpak/i386/share/applications /export/

	# Make binary available
	mkdir -p /app/bin
	cp -r app/.build/linux/flatpak/i386/share/code-oss/bin/* /app/bin

	# Add code-oss contents to the bundle
	cp -a app/.build/linux/flatpak/i386/share/code-oss /app

.PHONY: all install
