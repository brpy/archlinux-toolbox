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
## Stopping container

For some reason exiting toolbox does not stop the container. You can check running containers using `toolbox list`

Top stop container use `podman stop archlinux-toolbox`

---

This image is mainly intended for desktop use so it comes with `base-devel` as base package and `vim` installed.

To get a minimal image, build from parent repo. This is a fork of https://github.com/palazzem/archlinux-toolbox 
