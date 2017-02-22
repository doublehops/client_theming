# Instructions for branding Nextcloud client

## Application title
`rmpsystemstheme/OEM.cmake`

## Images
Wizard image: `rmpsystemstheme/theme/colored/wizard_logo.png` (132x63)
Retina wizard image: `rmpsystemstheme/theme/colored/wizard_logo@2x.png` (266x126)

Installer icon: `{OEM_THEME_DIR}/win/installer.ico` (32x32)

Welcome: `{OEM_THEME_DIR}/win/welcome.png` (164x314)

## Build
From build-linux path: (until I move outside)
`rm -rf * && cmake -D OEM_THEME_DIR=`pwd`/../rmpsystemstheme ../client && \
 make && \
 sudo make install`

## Run
`bin/nextcloud`

## Compile to binary
- for MacOSX
- for Windows

### Build and run Docker container / For Windows installer

Change line in win/build.sh to `-DOEM_THEME_DIR=/home/user/rmpsystemstheme \`

From root path:

- `sudo docker build -t nextcloud-client-win32:2.2 client/admin/win/docker/`
- `sudo docker run -v "$PWD:/home/user" nextcloud-client-win32:2.2 /home/user/win/build.sh $(id -u)`

This will build the Docker image to `build-win32/RMPSystems-2.2.4.0-setup.exe`.
