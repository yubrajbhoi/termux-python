# Python 3.12 for Termux

This is a fork of Python-3.12.1 with Termux patches (`termux.patch`) applied.

You can build with: `bash build.sh`

That will build and install it in `target` directory. You can install that directory with `stow` like this:

```
mkdir $PREFIX/stow
mv target $PREFIX/stow/python-3.12.1
cd $PREFIX/stow
stow -v --stow python-3.12.1
```
