PNGLua
======

A pure lua implementation of a PNG decoder

Usage
-----

To initialize a new png image:

    img = pngImage(<path to image>, newRowCallback)
    
The image will then be decoded. The available data from the image is as follows
```
img.width = 0
img.height = 0
img.depth = 0
img.colorType = 0

img:getPixel(x, y)
```
Decoding the image is synchronous, and will take a long time for large images.

Support
-------

The supported colortypes are as follows:

-    Grayscale
-    Truecolor
-    Indexed
-    Greyscale/alpha
-    Truecolor/alpha

So far the module only supports 8-bit Color. and no ancillary chunks.

Multiple IDAT chunks are supported, as well as all filters.