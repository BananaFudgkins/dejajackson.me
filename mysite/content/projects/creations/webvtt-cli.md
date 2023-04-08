---
title: "Webvtt CLI"
date: 2021-08-15T09:24:32-07:00
featured: false
description: "A command line tool for converting CSVs to VTTs."
image: ""
link: "https://github.com/LafayetteCollegeLibraries/webvtt-cli"
fact: "Interesting little tidbit shown below image on summary and detail page"
weight: 500
sitemap:
  priority : 0.8
---

I wrote this CLI in C++ while I was working with Skillman Library at Lafayette College. For our video captioning workflow, we wrote captions in a spreadsheet. To display subtitles over a video, this spreadsheet would need to be converted into an appropriate VTT file. This tool can take multiple CSV files as input and write them to separate VTT files that can be added to a video.

This tool can be installed via Homebrew as detailed by the readme [here.](https://github.com/LafayetteCollegeLibraries/homebrew-dss)