---
layout: page
title: Shutterbug
description: Variable Star Detection in Python
img: assets/img/nebula_spherical.jpg
importance: 1
category: work
related_publications: false
---

At the beginning of my internship with the Rothney Astrophysical Observatory, I was tasked with finding a way to procedurally generate graphs for star timeseries data from a .csv. From this project came <a href="https://github.com/AdaVoden/differential-photometry">Shutterbug</a>, an automated variable star detection tool.

Given an arbitrary Excel sheet or .csv with appropriate headers and data, it can automatically process photometric observations to remove atmospheric effects and applies statistical testing to identify potentially variable stars. It outputs graphs sorted by detection confidence.

Currently a commandline tool, with plans to add a GUI via PyQt.

## Technical Approach

Python was chosen as the language due to its frequent usage in scientific literature, my familiarity with it and the extremely powerful astronomical Python modules that have been released. With Pandas and Numpy, the speed of calculating thousands of stars can be measured to be under a second, so it was determined that Python was sufficiently fast as a language to perform all calculations and any other service that needed to be performed.

## Status

The project is functional and was actively used during my time at the RAO. README documentation is currently being expanded to include detailed installation and usage instructions.
