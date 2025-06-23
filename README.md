# Python 3.13 for Termux

This is a fork of Python-3.13.5 with Termux patches (`termux.patch`) applied.

But first make sure you have these dependencies installed with `apt` or `pkg`:

 - `python`, this will install all dependencies needed to build `python-3.13.5`
 - `build-essential`, this will install `clang`, `make` etc
 - `stow`, to install the package after building it

After that the package can be build with: `bash build.sh`. That will build and install it in `python-3.13.5` directory.

Or you can download the binary package from here:

 - [python-3.13.5-aarch64.tar.zst](https://public.8018985.xyz/python-3.13.5-aarch64.tar.zst)
 - [python-3.13.5t-aarch64.tar.zst](https://public.8018985.xyz/python-3.13.5t-aarch64.tar.zst)

`python-3.13.5t` is the free-threaded version. You can install that directory with `stow` like this:

```
mkdir -p $PREFIX/stow
mv python-3.13.5 $PREFIX/stow/
cd $PREFIX/stow
stow -v --stow python-3.13.5
```
