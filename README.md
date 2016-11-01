# lua2dox
Doxygen support for Lua files. Based on http://www.ctan.org/pkg/lua2dox

## Setup

In order to use Doxygen for parsing Lua files, perform the following installation steps:

1. Install the latest version of [Doxygen](http://www.stack.nl/~dimitri/doxygen/download.html).
1. Install the latest version of [Lua](https://sourceforge.net/projects/luabinaries/files).
1. Make sure both is in your path by running "doxygen" and "lua" from the command line.
1. Get the latest version of lua2dox.lua from the our GitHub page.
1. In your Doxygen file, set

```
EXTENSION_MAPPING = lua=C
FILTER_PATTERNS = *.lua=PATH\TO\lua2dox\lua2dox.lua
```

Now, running `doxygen` in a folder with Doxyfile will take every Lua input file, send it through lua2dox.lua, which in turn will convert the file to C-style syntax, which in turn is understood by Doxygen. 
