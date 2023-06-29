# Minilibx_WSL2
## Requirements
Let's start...
```
 sudo apt-get update && sudo apt-get upgrade -y
```
### Needed Packages
  - X11 (`sudo apt-get install xorg`)
  - Openbox `sudo apt-get install openbox`
- mesa-utils for glxinfo `sudo apt-get install mesa-utils`
- libxext-dev ``
- libbsd-dev
- run script to generate Makefile `./configure`

- configure [error] : Can't find a suitable X11 include directory.
make: *** [Makefile:17: do_configure] Error 1
```
sudo apt-get install libxext-dev
```
- /usr/bin/ld: cannot find -lbsd: No such file or directory
```
sudo apt-get install libbsd-dev -y
```
- ../includes/rt_render.h:19:11: fatal error: mlx.h: No such file or directory
   19 | # include <mlx.h>
      |           ^~~~~~~
```

```

## Download Minilibx
```
wget https://cdn.intra.42.fr/document/document/15731/minilibx-linux.tgz
tar xvf minilibx-linux.tgz
```
### OpenGL
Check if openGL is installed using `glxinfo` command.
- `glxinfo` can be found in mesa-utils package
```
sudo apt-get install mesa-utils
```
```
 glxinfo | grep "version"
```
