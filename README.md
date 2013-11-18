LCD Test Utilities
==================

This project is a collection of test images and a simple tool
to display images for Embedded Linux systems.  

Example
-------

* cmake ./
* display-image lcd-test.png

Motivation
----------

The project was born out of a need to be able quickly test LCD displays
in Embedded Linux systems.  It seemed I never had a quick way to display
a test image on a LCD.  Utilities that (eog) are normally used to do this have
a ton of dependencies.  The display-image utility only depends on Gtk2 and
its dependencies, which is typically available for most systems.  

Test Images
-----------

* lcd-test.png: simply gradients and color tests
* border.png: single pixel white line around the extents of the image.  This image is useful to verify
  you have the display alignment correct.  If it is shifted, they you will not see lines on all 4 sides.

Test images are generated using node-canvas.  To re-generate the images:

* make sure you have a recent version of node installed
* edit gen-images.js and enter your LCD size
* npm install
* node gen-images.js








