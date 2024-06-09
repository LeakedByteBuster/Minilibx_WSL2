# Minilibx_WSL2
# NOTES : 
    -L: Specifies the directory where the compiler should search for libraries.
        Example: -Lmlx_linux directs the compiler to search for libraries in the "mlx_linux" directory.

    -l: Specifies the name of a library that the compiler should link against.
        Example: -lmlx_Linux instructs the compiler to link against the library named "mlx_Linux".
         [ it expects the name without the lib prefix and the file extension. ]

    -I: Specifies an additional directory where the compiler should search for header files.
        Example: -Imlx_linux tells the compiler to search for header files in the "mlx_linux" directory.
        
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
