This repository is meant as an example of how to create a [G3D](https://casual-effects.com/g3d/www/index.html) starter project without having to modify your global visual studio user settings. 

The gist of the change from the default G3D starter is in [this changelist](https://github.com/jspjut/g3d-starter/commit/e1a78a0a012d021bf24d03513d681c1e62f61330).

You could also just copy this repository (mostly just the vcxproj and sln) to start your own project.

# Configure & Build

My updated instructions modified from the [G3D Configure and Build](https://casual-effects.com/g3d/G3D10/readme.md.html?#toc3.2) instructions follow below. You'll still need Visual Studio 2017 and an install of python 3 before the following.

1. Set your **user** or **system** environment variable `g3d` to the location that you'd like to be the
   root of the G3D tree (such as `c:\g3d`). In Windows 10, do this by &#9881; ==> System ==> About ==> System Info ==> Advanced System Settings ==> Environment Variables...
   (or by searching for "Environment Variables" in the start menu search)

2. Set the **user** or **system** environment variable `G3D10DATA` to
   `%g3d%\G3D10\data-files;%g3d%\data10\common;%g3d%\data10\game;%g3d%\data10\research`

3. SVN check out `https://svn.code.sf.net/p/g3d/code/` to `%g3d%`. This is very large, and likely to timeout if sourceforge has a hickup. Be prepared to `svn cleanup` and `svn up` if it doesn't finish

4. At a command prompt in the `%g3d%\G3D10` directory, run:
   
   `buildg3d local`

5. Copy my [g3d-starter](https://github.com/jspjut/g3d-starter) and follow the rest of the instructions from the [G3D new project guide](http://casual-effects.com/g3d/G3D10/build/manual/guidenewproject.html)

