fgallery 1.8.2: 25/05/2016
--------------------------

* Allow to generate a gallery directly on filesystems without hard-links.
* Fix generation failure on BSD systems (use a common set of "cp" arguments).
* Handle more malformed/missing EXIF timestamps.
* Use ``Cpanel::JSON::XS`` instead of ``JSON::XS`` (fixing errors in recent
  unsupported combinations of Perl / JSON::XS and threads).
* New ``fgallery`` man page provided by Guus Sliepen.


fgallery 1.8.1: 02/02/2016
--------------------------

* Fixed txt/xmp caption extraction for filenames with special characters.
* Fixed unicode handling in xmp/exif captions.


fgallery 1.8: 14/01/2016
------------------------

* Handle bogus whitespace in EXIF timestamps.
* Ignore hidden/invalid files instead of failing.
* Support ``tificc2`` as an alias to ``tificc`` (for Fedora).
* Avoid calling ``tificc`` for images already in sRGB.
* Load thumbnails on-demand for faster loading of large galleries.
* Extract and visualize image captions.
* Added ``utils/fcaption`` to edit image captions.


fgallery 1.7: 05/09/2014
------------------------

* Improved support for IE8.
* With Firefox the gallery can now be viewed directly without an HTTP server.
* Fixed crash when reading invalid EXIF timestamps.
* Fixed crash when reading read-only images.
* Fixed invalid check with newer versions of ImageMagick.


fgallery 1.6: 17/04/2014
------------------------

* Do not produce warnings when reading files without suffix.
* Strip EXIF metadata from image previews and thumbnails.
* We now require the ``Image::ExifTool`` perl module to extract EXIF
  information (``libimage-exiftool-perl``).
* Preview/thumbnail images are now converted to sRGB colorspace by default
  (``liblcms2-utils`` required) for improved color appearance across devices.
* Fixed mixing/sorting of images without EXIF data.
* A customizable URL (``--index``) can be specified on the command line to put
  a back-link in the gallery header.
* Reduced the payload size.


fgallery 1.5: 03/03/2014
------------------------

* Allow to reverse the album order (`-r`).
* Fixed crash when reading read-only images.
* Fixed crash when the input directory contains spaces.
* Fixed time sorting.


fgallery 1.4: 28/01/2014
------------------------

* Manual copying of the template directory is no longer required.
* Fixed incorrect thumbnail size for rotated JPGs.
* Fixed encoding of the album name.


fgallery 1.3: 05/01/2014
------------------------

* Improved browser behavior of the `back` button.
* Fixed incorrect thumbnail stretch for certain image ratios.
* Fixed empty thumbnail list in old browsers without ``devicePixelRatio``.
* Fixed incorrect usage of ``pngcrush``, resulting in stray PNG output files.
* Gallery generation speedup with parallelism/multi-core support (`-j`).
* Can use ``p7zip`` when installed for faster compression.
* Perl dependency on ``Date::Parse`` removed.
* Minor/cosmetic improvements.


fgallery 1.2: 30/11/2013
------------------------

* Faster loading of large galleries.
* Automatic thumbnail scaling on small screens.
* Improved support for mobile browsers.
* Swiping support.


fgallery 1.1: 21/10/2013
------------------------

* Degrades more gracefully on IE<10.
* Gallery generation speedup.
* Improved handling of UTF-8/special file names.
* Clicking on the main image shows the full image directly (if present).
* Adapts to the current screen layout automatically (horizontal/vertical layout).
* Supports face detection for improved thumbnail generation.
* JPEG/PNG optimization as an optional post-processing step.
* Minor/cosmetic improvements.
