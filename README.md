OpenGX
======

OpenGX is an OpenGL-like wrapper which sits on GX subsystem. It implements the most common OpenGL calls such as immediate mode, texturing, array drawing (indexed and not indexed), matrix operations and basic lighting. It features some advanced stuff such as automatic texture compression (ARB extension) and mipmapping. Beware! Some parts are currently NOT opengl compilant (speaking strictly).
TODO list

  * Fix lighting transform (which is buggy) and implement spotlights (untested)
  * Fix immediate mode to support arbitrary number of glVertex calls
  * Add more texture formats and/or add texture format conversion routines
  * Add freeglut or some SDL official patch to support context render creation (and remove manual initialization!)
  * Fix texture allocation. Now it's mandatory to allocate a texture name using glGen and you can't just bind the texture and use it
  * Complete glGet call
  * Add support for attribute push/pop
  * Add support for glReadPixels and similar calls
  * glError ang glGetString: add some error mechanism 

List of features (detailed but not exhaustive)

  * Texture conversion/compression. Accepts RGB,RGBA,COMPRESSED_RGBA and LUMINANCE_ALPHA.
  * Matrix math stuff including glu calls
  * Texture mipmapping (and gluBuildMipMaps)
  * Ambient and diffuse lighting. Looking forward to enable specular too. But note that 3 modes can't be used at the same time (HW restriction)
  * Indexed and not indexed draw modes
  * Blending support 
