SDLPAL
======

SDLPAL is an SDL-based reimplementation of the classic Chinese-language RPG
"Xian Jian Qi Xia Zhuan" (also known as PAL or Legend of Sword and Fairy).


LICENSE
=======

SDLPAL is originally created by Wei Mingzhi from 2009.
Copyright (c) 2009-2011 Wei Mingzhi <whistler_wmz@users.sf.net>.
Copyright (c) 2011-2016 SDLPAL development team.
All rights reserved.

SDLPAL is distributed under the terms of GNU General Public License, version 3
(or any later version) as published by the Free Software Foundation. See
gpl.txt for details.

Many of the ideas of this program are based on documents from PAL
Research Project (https://github.com/palxex/palresearch), and portions of the
code are based on the work done by Baldur and louyihua.

The resampler code is based on the code in Kode54's foo_input_adplug project
(https://github.com/kode54/foo_input_adplug).

This program made extensive use of the following libraries:

SDL (http://www.libsdl.org/)
Adplug (http://adplug.sourceforge.net/)
SDL_mixer (http://www.libsdl.org/projects/SDL_mixer/)
libmad (http://www.underbit.com/products/mad/)
libogg & libvorbis (http://www.vorbis.com/)
FLTK (http://www.fltk.org)

And some of the OPL simulation cores this program used are from the DOSBOX
project (http://www.dosbox.com) and MAME project (http://mamedev.org/).

Please see authors.txt for additional authors.

This program does NOT include any code or data files of the original game,
which is proprietary and copyrighted by SoftStar Inc.


COMPILE FOR WINDOWS
===================

The Microsoft Visual Studio 2013 or higher is supported under Windows.

To compile the WIN32 desktop version, open the Visual Studio project file 
'sdlpal.sln' under the 'win32' directory.

To comiple the WinRT version, open one of the project files (SDLPal.UWP.sln,
SDLPal.Windows.sln, SDLPal.WindowsPhone.sln) under the 'winrt' directory.
Please note that, to compile the UWP version, Visual Studio 2015 or higher
is required.

For all situations, you need to have SDL 2.0 development or source files 
installed at the SDL2 directory under the source tree.


COMPILE FOR GNU/LINUX OR UNIX
=============================

To compile, type:

cd unix
make

You need to have SDL 2.0 development files installed. The compiled executable
should be generated with the filename 'sdlpal' at the current directory. By
default, SDLPAL uses the FLTK library to provide setting GUI at launch. If you
do not want to use the library, please define the macro 'PAL_NO_LAUNCH_UI' in
the makefile.

SDLPAL should also be able to compile and run under other UNIX-like systems, 
however it's not tested.


COMPILE FOR MAC OS X
====================

To compile, open the project Pal.xcodeproj with Xcode, and click Build. You
need to have SDL framework installed at /Library/Frameworks.

COMPILE FOR IOS
===============

You need to have SDL2 source extracted in the SDL2 folder.To compile, 
open the project iOS/SDLPAL/SDLPal.xcodeproj with Xcode, and click Build. 


COMPILE FOR ANDROID
===================

You need to have SDL2 source extracted in the SDL2 folder.
To compile, type:
cd android/jni
ndk-build
cd ..
ant debug


COMPILE FOR OTHER PLATFORMS
===========================

To be written.


CLASSIC BUILD
=============

By default, SDLPAL uses a revised battle system which is more exciting yet
somewhat harder than the original game. If you prefer the traditional
turn-based battle system, uncomment the following line:

//#define PAL_CLASSIC           1

in the file common.h and recompile. This will build a "classic" build which is
100% the same as the original game.


RUNNING THE GAME
================

The data files required for running the game are not included with the source
package due to copyright issues. You must obtain them from the original CD.

To run the game, copy all the files on the original CD to a directory, then
copy the SDLPAL executable to the same directory, and run the executable.

Note that the filenames of data files should be in lower-case under GNU/Linux
(or other UNIX-like operating systems).


CONFIGURE THE GAME
==================

PAL has several variants using different and incompatible resource files. Now
SDLPAL supports several configuration options for supporting such variants.

To set these configuration options, create a file named as 'sdlpal.cfg' (make
sure to use lower-case file name in UNIX-like operating systems) in the game
directory created by the above step. If no configuration file exists, SDLPAL
uses default values that supports the original resources of DOS version.

Please refer to the 'sdlpal.cfg.example' for configuration file format.


-END OF FILE-
