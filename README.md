# Python 3.12 for Termux

This is a fork of Python-3.12.1 with Termux patches (`termux.patch`) applied.

## Install using binary package

Get the binary package from the releases page and install like this:

```
tar xf python-3.12.1-aarch64.tar.gz
mkdir $PREFIX/stow
mv python-3.12.1 $PREFIX/stow/
cd $PREFIX/stow
stow -v --stow python-3.12.1
```

## Build from source

First make sure you have these dependencies installed with `apt` or `pkg`:

 - `python`, this will install all dependencies needed to build `python-3.12.1`
 - `build-essential`, this will install `clang`, `make` etc
 - `stow`, to install the package after building it

After that the package can be build with: `bash build.sh`

That will build and install it in `target` directory. You can install that directory with `stow` like this:

```
mkdir $PREFIX/stow
mv target $PREFIX/stow/python-3.12.1
cd $PREFIX/stow
stow -v --stow python-3.12.1
```
