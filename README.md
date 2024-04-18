# alpaca's MTW2 .strings.bin converter, version 0.7
*Updated by SpyChicken18, version 0.1 (in development)*

## Content

1. Installation
2. Usage
3. Note
4. Changelog
5. License

## Installation

In order to use this tool, you need to download and install Python 3.0 or higher from [Python's Download Page](http://www.python.org/download).
Download and run the latest installer for Python that corresponds to the operating system of your computer (e.g. Windows, Mac, Linux).

After the installation of Python, place the script in your data/text directory (inside the folder where you unpacked the MTW2 files with CA's unpacker).

## Usage

After the installation, simply double click on the strings_bin_converter.py file to convert all convertible .strings.bin files to their .txt counterparts

### Options for advanced users
The script works using a list of filenames as command line options, so if you run the script from the command line, using the line
`strings_bin_converter_0_5.py export_buildings.txt`
it will only convert export_buildings.txt.strings.bin.
You can supply an arbitrary number of files, but it will generate an error if the filename is invalid.
You can supply a relative path to the directory of the converter.

If no arguments are provided, the script will convert all the files in the directory.

## Note on unconvertible files

This tool doesn't convert all .strings.bin files. The problem is that there are two types of these files.
Type 1 is untagged, which means that there's no good way to extract proper info out of this type of file (well at least not info the game would understand).
Type 2 is tagged though and this is what the converter tool can interpret and make useful info out of.
The reason for this is probably that they are staticly linked to stuff like buttons, and accessed by ID rather than by tag.

Files that are not converted:
battle.txt, battle_ed.txt, shared.txt, strat.txt, tooltips.txt

## Changelog

+ v0.1:
    + Copied alpaca's script to GitHub
    + Updated README

**All changes above this line refer to changes made by SpyChicken18, working from alpaca's version 0.72**  
**All changes below this line refer to changes made by alpaca to the original script written by alpaca**

+ v0.72:
    + Fixed the batch file
+ v0.71:
    + Removed the tab that went between description and tag for compatibility reasons
+ v0.7:
    + Fixed a bug with the line break character not being converted to \n, but written as a line break
+ v0.6:
    + Fixed a bug where the comment character wasn't written, this lead to the game not recognising the text file

## License

**Original License by alpaca**

You may freely redistribute altered or unaltered versions of this script, although for altered versions you have to mention this release in the read-me