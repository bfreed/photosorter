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
