libtcod-mac
===========

Mac OS X port of current development version of libtcod

Sorry, I need to get this better organized, but here are some basics.
Also note that this repo may be a few commits behind libtcod at this
point, but will get on that.

Build Instructions
==================

Assuming you are using homebrew on Mac OS X (tested only on 10.9,
10.10 I believe), there are a few dependencies. I *think* it is just
`cmake, sdl` and then for SDL2 it is `sdl2, sdl2_image`, although that
may be too many or too little. Please test.

Clone this repo with `git clone
https://github.com/podiki/libtcod-mac.git` and then `cd libtcod-mac`.
You can either build SDL1 with `make -f makefiles/makefile-osx
release` or SDL2 with `make -f makefiles/makefile-osx-sdl2 release`
(of course you can specify `debug` versions instead).

For the samples, simply do `make -f makefiles/makefile-samples-linux
release` or `make -f makefiles/makefile-samples-linux-sdl2 release`.
You will now have several example executables, which you can run as
`./hmtool`, `./samples_c`, or `./samples_cpp`.

Please test and report any issues and we can get this all up to speed.
Thanks!
