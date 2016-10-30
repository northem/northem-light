<p align="center"><img src="https://cdn.rawgit.com/arcticicestudio/northem-light/develop/src/assets/northem-light-logo-banner.svg"/></p>

<p align="center"><img src="https://assets-cdn.github.com/favicon.ico" width=24 height=24/> <a href="https://github.com/arcticicestudio/northem-light/releases/latest"><img src="https://img.shields.io/github/release/arcticicestudio/northem-light.svg"/></a> <img src="https://www.npmjs.com/static/images/touch-icons/favicon-32x32.png" width=24 height=24/> <a href="https://www.npmjs.com/package/northem-light"><img src="https://img.shields.io/npm/v/northem-light.svg"/></a> <a href="https://www.npmjs.com/package/northem-light"><img src="https://img.shields.io/npm/dt/northem-light.svg"/></a> <a href="https://www.npmjs.com/package/northem-light"><img src="https://img.shields.io/npm/dm/northem-light.svg"/></a></p>

---

# 2.0.1 (2016-10-30)
## Bug Fixes
### Sass
  - Fixed a compilation error caused by an malformed HEX code value of the `northem-light3` color variable during the Gulp task `compile-css-template` (@arcticicestudio, #10, 6c2ca65a7)
  - Added a missing recursive flag to the `cp` command for Circle CI build artifact processing

# 2.0.0 (2016-10-30)
**The milestone [Version 2.0.0](https://github.com/arcticicestudio/northem-light/milestone/2) release!**

The whole project has been rewritten and cleaned up to adapt to the new project setup like the [Nord](https://github.com/arcticicestudio/nord) project.

## Features
### Naming Scheme
**Color names**
The current naming scheme, where each color got an individual name based on the value, has been replaced with an numbered format.  
Example: `dark-gray` has been renamed to `northem-light0`, `gray` to `northem-light1`.  
This goes on with a continuous numerating where the current position of a color represents its number.

![Northem Light Palette Overview](https://cdn.rawgit.com/arcticicestudio/northem-light/develop/src/assets/northem-light-overview.svg)

**Components**
Next to this, the color palette has been divided into four named components to represent the different color effects where each component contains a different amount of colors:  
  1. **Dark Water** `northem-light0` - `northem-light3`  
  2. **Light Wind** `northem-light4` - `northem-light6`  
  3. **Ice** `northem-light7` - `northem-light10`  
  4. **Rainbow** `northem-light11` - `northem-light15`

This naming convention allows an uncomplicated use for terminals and preserves the compatibility to similar projects like [base16](chriskempson.com/projects/base16).

The X11 color scheme names and RGB value variables has been removed, but X11 color names are still included in the Sass- and LESSCSS source documentations.

### New color
A new color has been added to close the gap of the missing sixteenth color.  
The value of the color is `#E0E0E1` which has been added as `northem-light3` to the *Light Wind* component.  
This color is calculated from the color `northem3` (`#606062`) of the [Northem](https://github.com/arcticicestudio/northem) color palette via the Sass method `lighten($northem3, 50%)`.

### Source Formats
**Sass**
All [Sass](http://sass-lang.com) sources have been documented via [SassDoc](http://sassdoc.com) and a `template-css.scss` is available to be compiled to a CSS file including all color variables which is compatible to the CSS specification.  
The SassDoc is configurable via the `.sassdocrc` file.  
(@arcticicestudio, #4, 1f18eb02)

**LESSCSS**
All [LESSCSS](http://lesscss.org) sources have been documented via [KSS](http://warpspire.com/kss).  
(@arcticicestudio, #5, a1b22109)

**Native**
All native files have been recreated containing the new color and the new color naming scheme.  
(@arcticicestudio, #6, cdf2185e)
  
### Build Tools
**Gulp**
Introduced a [Gulp](gulpjs.com) file to compile Sass sources to CSS, provide a local hot-reload server for instant recompilatio on file changes and to build the new [SassDoc](http://sassdoc.com).  
(@arcticicestudio, #8, 6d958888)

**Travis CI and Circle CI**
Added the `.travis.yml` and `circle.yml` configuration files for continuous integration web services.  
(@arcticicestudio, #7, 102b498f)

### NPM
A `package.json` file has been added to provide project meta data and dependencies for a release as a [NPM](http://npmjs.com) package.  
(@arcticicestudio, #9, e8534a48)

### Assets
All project branding assets have been removed and replaced with new, modern SVG and AI files.  
(@arcticicestudio, #3, 256615dc)

### Documentations
All project documentations have been rewritten.  
The project license for the code has been changed to the [Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0) license.
(@arcticicestudio, #3, 256615dc)

### Git
The `.gitignore` and `.gitattributes` files have been rewritten to remove the high amount of unused pattern and comments.
(@arcticicestudio, #3, 256615dc)

# 1.0.1 (2016-05-06)
## Bug Fixes
### LESSCSS
  - Fixed a missing colon of the `@rgb-dark-snow` color variable (@zhrkevin, [GHI #6][ghi-6-arcticicestudio-northem-light-atom-syntax])
  - Removed leading whitespaces infront of the HEX and RGB color variables

# 1.0.0 (2016-04-16)
![Northem Logo](src/main/assets/media/northem-logo.png)

**Syntax Preview**  
![Northem Light Syntax Preview](src/main/assets/media/northem-light-syntax-preview.png)

## Features
### Native
  - Added the "[GIMP](https://www.gimp.org)/[Inkscape](https://inkscape.org) Palette" file format (`.gpl`)
  - Added the "[Adobe Swatch Exchange](https://helpx.adobe.com/illustrator/using/using-creating-swatches.html)" file format (`.ase`)
  - Added the "Alias/WaveFront Material" file format (`.mtl`)
  - Added the "[Gpick](http://www.gpick.org) Palette" file format (`.gpa`)
  - Added the binary exported [GIMP](https://www.gimp.org) XCF project image `northem-light.png` and `northem-light-large.png`
  ![Northem Large](src/main/native/northem-light-large.png)

### Non-Native
  - Implemented the [Sass](http://sass-lang.com) file format (`.scss`)
  - Implemented the [LESSCSS](http://lesscss.org) file format (`.less`)
  - Implemented the [JSON](http://json.org/) file format (`.json`)
  - Implemented the [XML](https://www.w3.org/XML) file format (`.xml`)

# 0.0.0 (2016-04-16)
*+Repository Reinitialization**

[backlog-application-support]: https://github.com/arcticicestudio/northem-light/issues/1

[ghi-6-arcticicestudio-northem-light-atom-syntax]: https://github.com/arcticicestudio/northem-light-atom-syntax/issues/6
