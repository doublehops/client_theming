# Instructions for branding Nextcloud client

## Application title
`rmpsystemstheme/OEM.cmake`

## Images
Wizard image: `rmpsystemstheme/theme/colored/wizard_logo.png` (132x63)
Retina wizard image: `rmpsystemstheme/theme/colored/wizard_logo@2x.png` (266x126)

Installer icon: `{OEM_THEME_DIR}/win/installer.ico`

## Build
From build-linux path: (until I move outside)
`rm -rf * && cmake -D OEM_THEME_DIR=`pwd`/../rmpsystemstheme ../client && make && sudo make install`


## Run
`bin/nextcloud`

## Compile to binary
- for MacOSX
- for Windows
