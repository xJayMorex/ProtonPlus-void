# ProtonPlus for Void Linux  
ProtonPlus template and builds for Void Linux.

![GitHub release (latest by date)](https://img.shields.io/github/v/release/xJayMorex/ProtonPlus-void?style=flat-square)

## Content Overview

- [**Building from sources**](#building-from-source)
- [**Binary release**](#binary-release)
    - [Available builds](#available-builds)
    - [Installing the binary package](#installing-the-binary-package)
- [**Credits**](#credits)

## Building from source

> **Note**
>
> *Consult void-packages [documentation][1] for more information about setting it up.*
>
> [*Quick start*][2]

## Binary release

### Available builds

Available builds:

- x86_64

### Installing the binary package

#### Method 1 - manual update

Download the `xbps` package from the [releases](//github.com/xJayMorex/ProtonPlus-void/releases) page, index and install the package:

```shell
xbps-rindex -a *.xbps
sudo xbps-install -vR $PWD protonplus
```

#### Method 2 - updates handled by xbps-install

Add the releases page as a repository:

```shell
cat << EOF > /etc/xbps.d/30-protonplus.conf
repository=https://github.com/xJayMorex/ProtonPlus-void/releases/latest/download
EOF
xbps-install -Su protonplus
```

First `xbps-install -S` run it will ask to import the repository key, same as [8e:9c:f9:9a:cd:77:2a:3c:25:54:61:c1:36:25:f0:4f.plist](void-packages/common/repo-keys/8e:9c:f9:9a:cd:77:2a:3c:25:54:61:c1:36:25:f0:4f.plist).

## Credits

- [ProtonPlus](//github.com/Vysp3r/ProtonPlus)
- [The Void source packages collection](//github.com/void-linux/void-packages)
- [The Void (Linux) distribution](//voidlinux.org/)

[1]:  //github.com/void-linux/void-packages/#readme
[2]: //github.com/void-linux/void-packages/#quick-start
