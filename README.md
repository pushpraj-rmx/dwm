# This is almost original software with following additional features, which were added using offical patches.

1. 'Systray'        (system tray)
2. 'Alpha'          (transparency)
3. 'C-Facts'        (to resie hight of individual windows, by defalut hight is divided equally)
4. 'Vanity gaps'    (control space between and around windows with keyboard shortcut instantly)
5. 'ScratchPad'     (Kind of floating windows which is ported to every workspace/...)
6. 'Xrdb'           (Xrdb support to change color directly from .Xresources file.)
7. 'Laucher'        (I don't personally use and its kind of bloat in here, I'll remove this in future updates)
8. MpdControl       (Control media playback from keyboard shortcut)

--------------------------------------------------------------------

dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
