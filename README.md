# How to set up Minetest server using Mac OS

## Download Luanti:

[Download Luanti](https://www.luanti.org/downloads/)

Open and follow instructions.
```sh
brew install --cask luanti
```

Open Terminal and type:

```sh
cd /Applications/Luanti.app
```

cd = change directory

brew = Homebrew (often just called "brew") is a popular package manager for macOS and Linux that makes it easy to install and manage software from the command line. It’s commonly used by developers to quickly set up tools, libraries, and command-line utilities.

ls = list 

```sh
cd Contents
cd MacOS
```

## Install Minetest:

```sh
cd
git clone https://github.com/minetest/minetest.git
cd ~/minetest
brew install cmake
brew install libogg libvorbis
cmake . -DRUN_IN_PLACE=TRUE -DBUILD_SERVER=TRUE
make -j$(sysctl -n hw.logicalcpu)
mv ./bin/luantiserver ~/minetestserver
```
