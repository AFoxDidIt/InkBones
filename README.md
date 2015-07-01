# InkBones
A Bone-Rigging Extension for Inkscape

InkBones is an attempt at developing a bone-rigging system for Inkscape vector graphics images.

##Problem Statement:

Inkscape is a powerful tool for graphics and artwork. However, it lacks bone-rigging, a feature that Professional Vector Graphics Animation Software ([Adobe Flash Professional](http://www.adobe.com/devnet/flash/articles/character_animation_ik.html), Anime Studio) and 3D Animation Software (Blender) software supports. As a consequence, creating poseable creations is difficult.

InkBones will be a tool to fix this. This system will be intended as an Extension of the Inkscape system - that is, a tool that Inkscape can use without recompiling its source code. This should additionally make it compatible with future builds of Inkscape.

## The Program

The program will be organized into three pieces:

### Inkbone Exporter
* An InkBone Exporter Extension, which grabs inkscape objects and outputs them as a skeleton. This will be selectable from a menu.
 
### Inkbone Editor
* An InkBone Editor, a system which positions bones as one desires them and outputs them. This will be a standalone app. Ideally, the program will be cross-plaform, so it should compile via Mingw or a cross-plaform compiler. However, the main developer only has access to Windows and Linux at the moment for testing, so OSX will unlikely be supported in the foreseeable future.

### Inkbone Renderer
* An InkBone Renderer, which applies transformations specified from the Editor.

## Core Principles:
* Inkscape is a black box - the Inkscape Extension should be plug-and-play wherever possible.
* Portability - the final app should not require special libraries to be installed on the system, thus being compatible with portable and installed Inkscape systems alike.
* Standardized Formatting: The bone structure output by the Exporter should be used by the Editor and Renderer whenever possible.
