# LEC — public downloads

Installers for the LEC desktop client. The source repository is private; this
repository exists only to host publicly downloadable builds.

## Latest: 1.0.3

Windows
- x64 (most PCs): https://web.lec.pxysio.top/updates/LEC-1.0.3-win-x64.exe
- arm64 (Windows on ARM): https://web.lec.pxysio.top/updates/LEC-1.0.3-win-arm64.exe
- sha512 (x64): `/oWZewb4rXJnMSBc21kG605VpDXLJ9XblQWgq8rnlXT/CxNpjoxmKFkx/gXh+XE8EM2389ni9bTtr8H4Dpml0w==`
- sha512 (arm64): `umj4ANMCP1FMSdOt5U2HgKpVhCc31YQjSE1yBX9JKtE255FOlO7cYsTkhEenOTj3HCf49u+aZRMfdI9IQqk+lQ==`

macOS
- Apple silicon: https://web.lec.pxysio.top/updates/LEC-1.0.3-mac-arm64.dmg
- Intel: https://web.lec.pxysio.top/updates/LEC-1.0.3-mac-x64.dmg

Linux
- AppImage: https://web.lec.pxysio.top/updates/LEC-1.0.3-linux-x86_64.AppImage
- deb: https://web.lec.pxysio.top/updates/LEC-1.0.3-linux-amd64.deb

## Install

Windows: run the `.exe`. It is not code-signed yet, so SmartScreen shows
"Windows protected your PC" - choose More info -> Run anyway. The installer lets
you pick the directory and creates desktop and start-menu shortcuts.

macOS: open the `.dmg`, drag LEC to Applications. Unsigned, so first launch needs
right-click -> Open, or `xattr -dr com.apple.quarantine /Applications/LEC.app`.

Linux: `chmod +x` the AppImage and run it (needs FUSE 2, or start it with
`--appimage-extract-and-run`), or install the `.deb`.

## Updates

Installed clients update themselves. The web UI reloads within about a minute of
a deploy, and the Electron shell is delivered by `electron-updater` from
`https://web.lec.pxysio.top/updates/` (manifests: `latest.yml`,
`latest-mac.yml`, `latest-linux.yml`) - it downloads in the background and
installs on the next quit. No reinstall is needed for normal fixes.