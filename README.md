# Python 3.13 for Termux

This is a fork of Python-3.13.6 with Termux patches (`termux.patch`) applied.

You can build from source or download the DEB packages from below. Unless you know how to build on Linux I would recommend the binary packages.

On some devices the binary packages might not work. In that case you will have to build from source.

## Build from source

First make sure you have these dependencies installed with `apt` or `pkg`:

 - `python`, this will install all dependencies needed to build `python-3.13.*`
 - `build-essential`, this will install `clang`, `make` etc
 - `stow`, to install the package after building it
 - `libandroid-spawn`, to get `spawn.h` header file

After that the package can be build with: `bash build.sh`. That will build and install it in `python-3.13.6` directory.

Or you can download a binary package from here:

## Binaries

All the files appended with `t` are the free-threaded version.

### DEB Packages

 - [python313_3.13.6_aarch64.deb](https://public.8018985.xyz/python313_3.13.6_aarch64.deb)
 - [python313_3.13.6t_aarch64.deb](https://public.8018985.xyz/python313_3.13.6t_aarch64.deb)

### Stow packages

 - [python-3.13.6-aarch64.tar.zst](https://public.8018985.xyz/python-3.13.6-aarch64.tar.zst)
 - [python-3.13.6t-aarch64.tar.zst](https://public.8018985.xyz/python-3.13.6t-aarch64.tar.zst)

### Python 3.14.0 Release Candidates

The source code is in `edge` branch.

 - [python-3.14.0rc1-aarch64.deb](https://public.8018985.xyz/python-3.14.0rc1-aarch64.deb)
 - [python-3.14.0rc1t-aarch64.deb](https://public.8018985.xyz/python-3.14.0rc1t-aarch64.deb)

 - [python-3.14.0rc1-aarch64.tar.zst](https://public.8018985.xyz/python-3.14.0rc1-aarch64.tar.zst)
 - [python-3.14.0rc1t-aarch64.tar.zst](https://public.8018985.xyz/python-3.14.0rc1t-aarch64.tar.zst)

## How to install

The easiest way to install is with the DEB files. Simply download a package and install like this:

```
apt install ./*.deb
```

You can also install with `dpkg` if you know how to resolve dependency errors:

```
dpkg -i *.deb
# To install missing deps
apt -f install
```

These deb packages can be uninstalled as usual like this:

```
apt remove python313
```

You can also install with stow, but it requires a little technical knowledge about how Linux directories work. First download and untar a stow package. You can also use the built from source directory. Replace `package_name` below with the directory use get.

```
mkdir -p $PREFIX/stow
mv package_name $PREFIX/stow/
cd $PREFIX/stow
stow -v --stow package_name
```

The packages installed with stow can be uninstalled like this:

```
stow -v --delete package_name
```

## Verify your installation

If you are using the free-threaded version append a `t` to every command. For example `python3.13` with `python3.13t`.

To install `pip` for this python installation you need to run `python3.13 -m ensurepip` once. After that you can use `pip` normally.

```
python3.13 --version
```
