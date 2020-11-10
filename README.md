![GitHub Workflow Status](https://img.shields.io/github/workflow/status/HedgeHawk/v4l2ucp/CMake)

# v4l2ucp
v4l2ucp - A universal control panel for all Video for Linux Two (V4L2) devices.

This is port of an original v4l2ucp to Qt5 library. Original version was written 
by Vasily Khoruzhick and Scott J. Bertin.

This software is written in C++ using Qt5 libraries on Linux. It reads a
description of the controls that the V4L2 device supports from the device,
and presents the user with a graphical means for adjusting those controls.
It allows for controlling multiple devices. There is an easy way
to reset one or all the controls to their default state.

A list of device files can be given on the command line. If no files are
given, the program will check the V4L2UCP_DEV environment variable. If it
is set, that file will be opened. Finally, it will try to open /dev/video0
if nothing else was specified. If no devices can be opened, the program will
exit.

In addition to the standard Qt arguments, v4l2ucp will also recognize -h and
--help. These will print a brief usage summary and exit.

To build this software invoke:
mkdir build
cd build
cmake ..
make
