# find-manual-installed-local-deb-package


## Intro

Bash script to find all manually installed local deb-packages.

Steps to find these packages:

1. Remove all old package lists in /var/lib/apt/lists/
2. Update all packe lists from current sources.list, i.e. run apt-get update
3. Find all currently installed packages.
4. Find all available packages from updated /var/lib/apt/lists - files.
5. Find all packages that are found in step 3 BUT NOT found in step 4 (difference set of installed packages and available packages)

Note: Step 1 and Step 2 need root privileges.

## Installation

Clone

    git clone git@github.com:pepe79/find-manual-installed-local-deb-package.git

OR Download

    wget -O find-manual-installed-local-deb-package.zip https://github.com/pepe79/find-manual-installed-local-deb-package/archive/master.zip
    unzip find-manual-installed-local-deb-package.zip
    rm find-manual-installed-local-deb-package.zip

## Usage

    cd find-manual-installed-local-deb-package
    chmod a+x find-manual-installed-local-deb-package.sh
    ./find-manual-installed-local-deb-package.sh


## Example output 

    Updating package information...
    Locally installed packages outside of current apt-get sources list:

    android-studio
    code
    google-talkplugin
    hll2340dcupswrapper
    hll2340dlpr
    icaclient
    libpng12-0
    libvpx1
    linux-headers-4.3.3-040303
    linux-headers-4.3.3-040303-generic
    linux-image-3.19.0-31-generic
    linux-image-4.3.3-040303-generic
    linux-image-extra-3.19.0-31-generic
    primetime
    spotify-client
    sublime-text
    virtualbox-5.1
    zoom

