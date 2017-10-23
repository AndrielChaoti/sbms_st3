# Starbound Modding Suite for Sublime Text 3
This is a Sublime Text 3 collection of packages that will help make modding for
Starbound that much easier

## Coming Soon
- GOG build support
- A way to automatically detect if your current open project is a Starbound project or not (Probably by the `_metadata` file.)


## Installation
### Included in the package:
- Starbound
    - JSON syntax highlighter associated with the Starbound asset files
    - Lua syntax highlighter with auto complete suggestions for base tables
    - A build system for running the game and watching log output
    - snippet for building \_metadata files
- Additional
    - Extra packages
        - SublimeLinter
        - SublimeLinter-lua
        - SublimeLinter-json
        - SublimeLinter-annotations
        - PackageResourceViewer
    - Sublime Preferences (optional: There are a few useful settings you may like, but this is *my personal* setup)
    - SublimeLinter Preferences (Optional, enables tool-tips and sets a reasonable highlight mode. **mostly default otherwise**)

### Steps
1. Open Sublime Text 3
2. Preferences > Browse Packages
3. Copy the entire **Starbound** folder over to your Sublime Text package directory
4. In the **User** folder, if you have it installed, open **Package Control.sublime-settings**  
    **If you don't have Package Control installed:**
    1. Press <kbd>CTRL</kbd>+<kbd>SHIFT</kbd>+<kbd>P</kbd> to open the Command Pallete
    2. Type "Package Control" into the search box
    3. Press <kbd>Return</kbd> when "Install Package Control" is selected.  
        Package Control will open a new tab when it's successfully installed.

    **With Package Control Installed:**

    - Add the contents of my **Package Control.sublime-settings** to yours.  
        ***Note:** You can overwrite the entire file if you wish.*  
        *The other option is to manually install the packages listed in the file.*  
    - Should look something like this:
```json
{
    "bootstrapped": true,
    "in_process_packages":
    [
    ],
    "installed_packages":
    [
        "Package Control",
        "PackageResourceViewer",
        "SublimeLinter",
        "SublimeLinter-annotations",
        "SublimeLinter-json",
        "SublimeLinter-lua",
        /* Any additional packages you had installed beforehand go here */
    ]
}
```
5. ***Restart Sublime Text***. This is required only if you manually edited **Package Control.sublime-settings**
6. **(Optional)** You can copy the contents of the **Preferences.json** file if you wish.
    - Lines that are commented out (they start with `//`) are my personal preferences
    - Lines that aren't, however, are recommended settings.
7. **(Optional)** Edit or overwrite SublimeLinter settings.
    - Key settings for Starbound modding are as follows:
    - Json Lint `"strict": true,`
    - Under `"syntax_map"`, add the following lines:
        - `"starbound lua": "lua",`
        - `"starbound json": "json"`
8. **(Optional)** Add Linter Executables:
    - I have included a Lua 5.3 binary for Windows users in the package, but some users would prefer their own, or are not on Windows. [Lua-users Wiki](http://lua-users.org/wiki/LuaBinaries) has a list of places where you can find binaries for your specific OS.
    - Follow the instructions on [finding a linter executable](http://sublimelinter.readthedocs.io/en/latest/troubleshooting.html#finding-a-linter-executable) to properly set up SublimeLinter.
        - **The JSON linter is built-in to Sublime Text, you will only need to provide `luac` for the Lua linter.**

Once you've completed all of that, you should be good to go. Open up the files from your favorite Starbound mod and get hacking!

## [DocParser_Release.7z](https://github.com/AndrielChaoti/docparser)
I've included the program that I used to generate the `starbound.sublime-completions` file, so that if horrible things happen, you won't be left hanging in the dust, or manually updating the file. It parses through Starbound's Lua documentation, and reformats the lines matching function names into proper Sublime Text completion objects.

The software is compiled for Windows 64-bit, against .NET Framework 4.6.1, and written in C#. It is fully Mono compatible. Since it's mostly a debugging tool, I don't really expect you to use it. Call the program with no arguments to get help on how to properly use it.

## Caveats and Incompatibilities
***Most*** of the tools should work on any system, and with some minor modifications to paths in some files, they should be able to be configured to work on your specific system too!

If you have any major issues, feel free to make an issue report.

## Additional Software Licenses
Software that is included in this package is used (hopefully) with permission from the authors, the licenses for any additional software packages are below.
### Lua
Copyright © 1994–2017 Lua.org, PUC-Rio.
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sub license, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
