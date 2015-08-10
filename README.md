photosorter
===========

A QGIS plugin to sort photos and link them to associated map nodes

Why
===
Often, people take photos of a group of things and then want to show those things on a map.
This seems to be fairly common across many industries. Personally, I've observed this need with drainage structures, E&S BMPs, utility poles, and (most recently) exterior lighting fixtures.

I would expect that many people have solved this problem programatically. Oddly, I have not found anything else similar.
If anyone reading this knows of one, please let me know.

A friendly nod to history
=========================
I coined the phrase "PhotoSorter" at Katapult Engineering (www.katapultengineering.com) for a QGIS plugin that started with the same capabilities as this plugin, then grew to include much more. However, that version: a) is fundamentally about collecting utility poles and wires and could not be easily generalized, b) is no longer called "PhotoSorter" but is a small part of a differently-named plugin used internally, and c) is not publicly available.

This plugin will be written from scratch and will share no code with the previous one, so no attribution is necessary. I mention it nonetheless because if you happen to be planning to inventory utility poles, you should stop reading now and immediately call Katapult. The goal of this plugin is to be generally useful -- it will never be as efficient as Katapult's internal tools at the same narrow problem set they solve.

The plan
========
I will build this plugin in stages. While I'd like to say I'll develop & maintain it forever, I won't. Realistically, development will continue until it meets my goals or until I am gainfully employed somewhere else, whichever happens first.
**UPDATE: gainful employment happened first. This project never started and probably never will.**

Stage 1 "basically helpful" goals:
- create image thumbnails, display them in filename order (format SD cards before starting!)
- allow a selected group of photos to be assigned to a point object on the map
- will require Spatialite database with "nodes" and "node_photos" tables
- will store full paths in node_photos table

Stage 2 "very helpful" goals:
- read date taken and GPS from EXIF data
- display thumbs in the order taken (regardless of filename numbering rollover)
- display embedded GPS (if any) on the map canvas

Stage 3 "basic options" goals:
- allow user-specified table names
- allow choice of full path, relative path, or filename-only 

Stage 4 "multiple camera" goals:
- given multiple cameras that each took a photo of the same clock (the "sync" photo):
- correct for differences in camera device clocks
- display images from the directories feathered together, in order of (corrected) time taken

Unlikely but conceivable:
- support data formats other than Spatialite
- export node data & filenames to CSV (Spatialite-GUI does this, but requires building from source for Linux or Mac OS)
- package project into KML/KMZ with embedded image links, for consumption in Google Earth
