VAMDC-tutorials
===============

Collected material for tutor-led and self-taught tutorials.

This repository contains Sphinx source for a web-site to present the tutorial materials.

To build the web pages, run "make html"; the web-site will be delivered in the directory build/html. 
This operation requires Sphinx to be installed on the computer where make is executed.

A Dockerfile is included to run the web site in NGINX: i.e. it builds the tutorial content
into a Docker image based on NGINX. To build this image, first run make to generate the
web-site content in build/html; the Dockerfile picks it up from there.

