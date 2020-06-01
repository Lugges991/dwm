# lugges' dwm - lugges' build of the suckless dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.


## Requirements
------------
In order to build dwm you need the Xlib header files.
Furthermore "DeJa Vu Sans Mono Nerd Font" is required, which can be changed though.
To launch a terminal with the default configuration, the suckless st terminal is required.


## Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


## Running dwm
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


## Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.


## Features
-------------
* Stacked tiling
* Centered master tiling
* Floating mode

## Keyboard Shortcuts
-------------
The following keyboard shortcuts are used to operate dwm:

| Shortcut                  | Function                  |
|---------------------------|---------------------------|
| Alt + j                   | Increase focus            |
| Alt + k                   | Decrease focus            |
| Alt + Return              | Change focus              |
| Alt + Shift + Return      | Spawn terminal            |
| Alt + p                   | launch dmenu_run          |
| Alt + Tab                 | Cycle Workspace           |
| Alt + q                   | Kill current window       |
| Alt + t                   | tiling mode               |
| Alt + f                   | floating mode             |
| Alt + m                   | monocle mode              |
| Alt + u                   | centered master           |
| Alt + o                   | centered floating master  |
| Alt + ,                   | cycle layout increasing   |
| Alt + ,                   | cycle layout decreasing   |
| Alt + Space               | set previous layout       |
| Alt + Shift + Space       | set previous layout       |
| Alt + [1..9]              | switch to workspace [1..9]|
| Alt + 0                   | view all workspaces       |
| Alt + Shift + 0           | tag all workspaces        |
| Alt + ,                   | switch monitor            |
| Alt + .                   | switch monitor            |
| Alt + Shift + ,           | tag monitor               |
| Alt + Shift + .           | tag monitor               |
| Alt + F5                  | refresh x-colors          |
| Alt + Shift + q           | Exit dwm                  |
| Alt + +                   | Increase all gaps         |
| Alt + -                   | Decrease all gaps         |
| Alt + Super + +           | Increase outer gaps       |
| Alt + Super + -           | Decrease outer gaps       |
| Alt + Shift + +           | Increase inner gaps       |
| Alt + Shift + -           | Decrease inner gaps       |
| Alt + Super + 0           | toggle gaps               |
| Alt + Super + Shift       | reset gaps                |
*** Work in Progress ***
