LCD Test Utilities
==================

This project is a collection of test images and a simple tool
to display images for Embedded Linux systems.  

Example
-------

* cmake ./
* ./lcd-test images/lcd-test.png


Cross Compiling
---------------

If you are using OpenEmbedded, use the following recipe:

https://github.com/cbrake/meta-bec/blob/master/recipes/lcd-test/lcd-test\_git.bb

Motivation
----------

The project was born out of a need to be able quickly test LCD displays
in Embedded Linux systems.  It seemed I never had a quick way to display
a test image on a LCD.  Utilities (oeg) that are normally used to do this have
a ton of dependencies.  The display-image utility only depends on Gtk2 and
its dependencies, which is typically available for most systems.  

Test Images
-----------

* lcd-test.png: simple gradients and color tests.  Also includes a 1px white line
  around the border that can be used to check alignment.

Test images are generated using node-canvas.  To re-generate the images:

* make sure you have a recent version of node installed
* edit gen-images.js and enter your LCD size
* npm install
* node gen-images.js
* TODO








