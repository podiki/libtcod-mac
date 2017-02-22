# **Can now build directly (this repository no longer needed)** #

With a working [Homebrew](https://brew.sh/) installation, `brew install autoconf automake libtool pkg-build sdl2`. To build from the current development version of [libtcod](https://bitbucket.org/libtcod/libtcod) (rather than [downloading](https://bitbucket.org/libtcod/libtcod/downloads/) a source package), `brew install mercurial`. Then follow the [directions](https://bitbucket.org/libtcod/libtcod/src/113b84f4fea8ba262f5d4a34136a0b88b43fa053/README-linux-SDL2.md?fileviewer=file-view-default) for building libtcod 1.6 (just the final section). Note that the actual libraries will be in `libtcod/build/autotools/.lib`, with several symlinks.

As of this writing, this has been tested on the 1.6.3 development version of libtcod with macOS 10.12.3. Samples and Python bindings (e.g. from the ["Complete Roguelike Tutorial, using python+libtcod"](http://www.roguebasin.com/index.php?title=Complete_Roguelike_Tutorial,_using_python%2Blibtcod)) all work as expected from brief testing.

(I will keep this repository up for now, but please refer to upstream libtcod for all questions and issues. Below is the original readme.)

-------------------------------------------------------------------------------

## libtcod-mac ##

Mac OS X port of current development version of [libtcod](https://bitbucket.org/libtcod/libtcod)

Sorry, I need to get this better organized, but here are some basics.
Also note that this repo is behind upstream libtcod at this
point. I no longer have a Mac to maintain or update this port,
so it would be great if someone can pick it up (see [Issue #4](https://github.com/podiki/libtcod-mac/issues/4)).

## Build Instructions ##

Assuming you are using homebrew on Mac OS X (tested only on 10.9,
10.10 I believe), there are a few dependencies. I *think* it is just
`cmake, sdl` and then for SDL2 it is `sdl2, sdl2_image` (although this
may be too many or too little). The samples also require `upx`. Please
test.

This has been tested with SDL2, but should work with SDL1 as well.
You have to change an include path, see [Issue #9](https://github.com/podiki/libtcod-mac/issues/9).

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
