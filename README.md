# Archlinux Toolbox

Archlinux toolbox that can be used with [Toolbox](https://github.com/containers/toolbox).


## Usage on Fedora

```bash
$ sudo dnf install buildah podman toolbox
$ git clone https://github.com/brpy/archlinux-toolbox.git
$ cd archlinux-toolbox
$ buildah bud -t archlinux
$ toolbox create -i localhost/archlinux:latest -c archlinux-toolbox
$ toolbox enter -c archlinux-toolbox

# You should see this but with your username:
# [palazzem@toolbox ~]$
```
