alpaca's MTW2 .strings.bin converter, version 0.7

Content:
------------------------------------------------------------------

1. Installation

2. Usage

3. Note

4. Changelog

5. License

------------------------------------------------------------------

1. Installation

In order to use this tool, you need to download and install Python 2.5 from http://www.python.org/download first
What you are searching for is probably the "Python 2.5 Windows installer", so if you're unsure, just download and install this.

After the installation of Python, extract this archive to your data/text directory (inside the folder where
you unpacked the MTW2 files with CA's unpacker).


------------------------------------------------------------------

2. Usage

After the installation, simply run convert_all.bat to convert all convertible .strings.bin files to their .txt counterparts

Options for advanced users:

The script works using a list of filenames as command line options, so if you run the script using the line
strings_bin_converter_0_5.py export_buildings.txt
it will only convert export_buildings.txt.strings.bin, you can supply an arbitrary number of files, but it will generate an error if the filename is invalid.
You can supply a relative path to the directory of the converter.

The commandline option "all" extracts all .strings.bin files in the script directory, see the batch file for an example


------------------------------------------------------------------

3. Note

This tool doesn't convert all .strings.bin files. The problem is that there are two types of these files, type 1 is untagged, which means that there's no good way
to extract proper info out of this type of files (well at least not info the game would understand), 
type 2 is tagged though and this is what the converter tool can interpret and make useful info out of.
The reason for this is probably that they are staticly linked to stuff like buttons, and accessed by ID rather than by tag.

Files that are not converted:
battle.txt, battle_ed.txt, shared.txt, strat.txt, tooltips.txt


------------------------------------------------------------------

4. Changelog

v0.72:
- Fixed the batch file
v0.71:
- Removed the tab that went between description and tag for compatibility reasons
v0.7:
- Fixed a bug with the line break character not being converted to \n, but written as a line break
v0.6:
- Fixed a bug where the comment character wasn't written, this lead to the game not recognising the text file


------------------------------------------------------------------

5. License

You may freely redistribute altered or unaltered versions of this script, although for altered versions you have
to mention this release in the read-me