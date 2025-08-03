# rman-amiga

This is rman (AKA PolyglotMan), compiled for classic Amiga, without ixemul or other POSIX dependencies, and with additional AmigaGuide support.

## [amigazen project](http://www.amigazen.com)

*A web, suddenly*

*Forty years meditation*

*Minds awaken, free*

**amigazen project** uses modern software development tools and methods to update and rerelease classic Amiga open source software. Our upcoming releases include a new AWeb, and a new Amiga Python 2.

Key to our approach is ensuring every project can be built with the same common set of development tools and configurations, so we created the ToolKit project to provide a standard configuration for Amiga development. All *amigazen project* releases will be guaranteed to build against the ToolKit standard so that anyone can download and begin contributing straightaway without having to tailor the toolchain for their own setup.

The original authors of the *rman* software are not affiliated with the amigazen project. This software is redistributed on terms described in the documentation, particularly the files COPYING or LICENSE.md

Our philosophy is based on openness:

*Open* to anyone and everyone	- *Open* source and free for all	- *Open* your mind and create!

PRs for all of our projects are gratefully received at [GitHub](https://github.com/amigazen/). While our focus now is on classic 68k software, we do intend that all amigazen project releases can be ported to other Amiga-like systems including AROS and MorphOS where feasible.

## About ToolKit

**ToolKit** exists to solve the problem that most Amiga software was written in the 1980s and 90s, by individuals working alone, each with their own preferred setup for where their dev tools are run from, where their include files, static libs and other toolchain artifacts could be found, which versions they used and which custom modifications they made. Open source collaboration did not exist as we know it in 2025. 

**ToolKit** from amigazen project is a work in progress to make a standardised installation of not just the Native Developer Kit, but the compilers, build tools and third party components needed to be able to consistently build projects in collaboration with others, without each contributor having to change build files to work with their particular toolchain configuration. 

All *amigazen project* releases will release in a ready to build configuration according to the ToolKit standard.

Each component of **ToolKit** is open source and like *rman* here will have it's own github repo, while ToolKit itself will eventually be released as an easy to install package containing the redistributable components, as well as scripts to easily install the parts that are not freely redistributable from archive.

## Features

- **AmigaGuide Output**: Convert man pages to native AmigaGuide (.guide) format
- **Multiple Output Formats**: HTML, ASCII, RTF, LaTeX, XML, and more

### Build Commands

```bash
# Build the executable
smake

# Clean build files
smake clean

# Create binary release archive
smake archive

# Test AmigaGuide conversion
smake test-guide
```

## Usage

```bash
# Convert man page to AmigaGuide format
rman -f AmigaGuide input.1 > output.guide

# Convert to HTML
rman -f HTML input.1 > output.html

# Convert to ASCII text
rman -f ASCII input.1 > output.txt
```

### Available Output Formats
- `AmigaGuide` - Native Amiga documentation format
- `HTML` - Web browser format
- `ASCII` - Plain text format
- `RTF` - Rich Text Format
- `LaTeX` - LaTeX document format
- `XML` - XML format
- `roff` - Troff format
- `TkMan` - TkMan format

## About AmigaGuide Export

The generated .guide files include:
- Proper AmigaGuide syntax (@database, @node, etc.)
- Navigation links
- Formatted text with bold, italic, and monospace
- Table of contents
- Cross-references

## Requirements

- Amiga or Amiga-compatible computer with latest operating system software
- SAS/C 6.58 setup according to ToolKit standard

## Installation

- copy SDK/C/rman to SDK:C/ this being the standard location for ToolKit commands
- make sure SDK: exists as an assign to your ToolKit files root, and that SDK:C/ is in your path
- the ToolKit sdk-startup script will do this for you if you have it installed
- rman can also be used standalone, in which case simply place the *rman* binary somewhere in your path

## Changelog

- Modified smakefile to build against ToolKit standards
- Completely refactored AmigaGuide export code

## To Do

- Further enhancements to AmigaGuide output
- Add VBCC makefile support

## Contact 

- At GitHub https://github.com/amigazen/rman-amiga
- on the web at http://www.amigazen.com/toolkit/ (Amiga browser compatible)
- or email toolkit@amigazen.com

## [Aminet.readme](https://www.aminet.net/package/text/misc/rman)

***N.B. this readme contents dates to 2007! contact details may no longer be relevant!***

PolyglotMan takes man pages from most of the popular flavors of UNIX and
transforms them into any of a number of text source formats. PolyglotMan
was formerly known as RosettaMan. The name of the binary is still called
rman , for scripts that depend on that name; mnemonically, just think
"reverse man". Previously PolyglotMan required pages to be formatted by
nroff prior to its processing. With version 3.0, it prefers [tn]roff source
and usually produces results that are better yet. And source processing is
the only way to translate tables. Source format translation is not as
mature as formatted, however, so try formatted translation as a backup.

## Acknowledgements

*Amiga* is a trademark of **Amiga Inc**. 

Original rman (AKA PolyglotMan) is Copyright (C) Tom Phelps
AmigaGuide support added by Chris Young 2007
Released under the Artistic License see [LICENSE.md]