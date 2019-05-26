# bgs - back ground setter
bgs is an extremely fast and small background setter for X. This fork of bgs fixes a few bugs and added support for automatic EXIF detection.


## Requirements
In order to build bgs you need the Xlib, Imlib2, and libexif header files.


## Installation
Edit config.mk to match your local setup (bgs is installed into the /usr/local namespace by default).

Afterwards enter the following command to build and install bgs (if necessary as root):

    make clean install


## Running bgs
Add the following line to your .xinitrc to start bgs using startx:

    bgs <image> &

In order to connect bgs to a specific display, make sure that the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 bgs <image> &

(This will start bgs on display :1 of the host foo.bar.)

In order to have a different image on each monitor you can specify multiple images (one per monitor), e.g.:

    DISPLAY=foo.bar:1 bgs <image1> <image2> &

(This will display image1 on monitor 1 and image2 on monitor 2.)
