#Security Advancement for multi VNC Server usage

This is a security advancement for [LibVNCServer](http://libvncserver.sourceforge.net/).
Intersting changes are in [`storepasswd.c`](https://github.com/johannesboyne/libvncserver/blob/master/examples/storepasswd.c#L68), `rfb/rfbproto.h` and `common/vncauth.c`.

##Why a security advancement

If you want to use LibVNCServer multiple times you should change the behaviour of the `storepasswd` program and use custom salted passwords.

##How to build

*The prerequisites:*

The usual C compiler with headers and stuff.
For the more advanced VNC encodings: zlib and libjpeg development packages.
If you want to try out the provided client example: libSDL development package version >= 1.2.0.

To configure the source:
On Unix/Linux platforms, just the usual:

```
./configure
make
```

##What is it?

VNC is a set of programs using the RFB (Remote Frame Buffer) protocol. They
are designed to "export" a frame buffer via net (if you don't know VNC, I
suggest you read "Basics" below). It is already in wide use for
administration, but it is not that easy to program a server yourself.

##License

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA  02111-1307, USA.dfdf

##Previous Author

Copyright (C) 2001-2003 Johannes E. Schindelin
