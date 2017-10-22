# Starbound Modding Suite for Sublime Text 3
This is a Sublime Text 3 collection of packages that will help make modding for
Starbound that much easier

## Includes
- A build system for launching Starbound and viewing log output live in the console window.
	- 64-bit Windows
	- Linux
	- Steam Protocol
	- 32-bit Windows
	- ~~GOG Installations~~ *not supported yet*
	- ~~Mac OS Installations~~ *not supported yet*
- Autocomplete definitions for all of the Starbound Lua API
- Syntax Highlighting for Lua and JSON files used by Starbound
- Snippets of code that can help make developing new mods easier
	- \_metadata file template.

## Coming Soon
- GOG build support
- MacOS build support
- Seperate Syntax Highlighting languages for Starbound Mods
	- These will be copies of the built-in Sublime themes, just with a different name, so as to not
	conflict with existing projects that don't need this
	- JSON syntax-specific settings will also change to be for Starbound JSON, instead of also normal JSON
- A way to automatically detect if your current open project is a Starbound project or not (Probably by the `_metadata` file.)


## Installation
Need to get up and running quickly? The most basic installation is to just drag and drop the contents of this archive into your Sublime Text 3 **Packages** directory. For a bit more advanced setup, such as not stomping over files you already have, follow the guide below

- Start Sublime Text 3.
- Open your packages directory by selecting **Packages** > **Browse Packages...** from the menu.
- Copy the contents of the **User** directory into this new window.
	- Advanced: Instead of completely overwriting your `Package Control.sublime-settings` file, open it up in Sublime Text. Copy the contents of the `Package Control.sublime-settings` file provided (From the `installed_packages` key only), and add them to your list of installed packages
- Navigate up one level. You should be in `/Packages` not `/Packages/User`
- Copy the **Starbound** folder to your Packages directory

That's it for basic setup. To enable linting of Lua files, you'll need to extract the lua archive somewhere on your system's `PATH`. For Windows users, extract the contents of the **lua-[version].7z** to a folder on your `C:\` drive. Lua binaries are always available for download at [the lua-users wiki](http://lua-users.org/wiki/LuaBinaries).

When setting up the executable for SublimeLinter, you can follow the instructions on [finding a linter executable](http://sublimelinter.readthedocs.io/en/latest/troubleshooting.html#finding-a-linter-executable). Instructions are also available here on how to set it up if you don't know how!

### Installing Lua on Linux
Lua binaries are available online for free, but they are also available in your
favourite package manager as well:

#### Ubuntu:
```bash
 # apt install lua-5.3
```

#### Other Linux Distros
For other Linux distros, you can find and download your specific Lua implementation at [the lua-users wiki](http://lua-users.org/wiki/LuaBinaries). There are also instructions there that can guide you through building your own Lua binaries.

## [DocParser_Release.7z](https://github.com/AndrielChaoti/docparser)
I've included the program that I used to generate the `starbound.sublime-completions` file, so that if horrible things happen, you won't be left hanging in the dust, or manually updating the file. It parses through Starbound's lua documentation, and reformats the lines matching function names into proper Sublime Text completion objects.

The software is compiled for Windows 64-bit, against .NET Framework 4.6.1, and written in C#. It is fully Mono compatible. Since it's mostly a debugging tool, I don't really expect you to use it. Call the program with no arguments to get help on how to properly use it.

## Caveats and Incompatibilites
***Most*** of the tools should work on any system, and with some minor modifications to paths in some files, they should be able to be configured to work on your specific system too!

## Legal
### Licence
MIT Licence

Copyright (c) 2017 Donald "AndrielChaoti" Granger

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Additional Software
Software that is included in this package is used (hopefully) with permission from the authors, the licences for any additional software packages are below.
#### Lua
Copyright © 1994–2017 Lua.org, PUC-Rio.
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
