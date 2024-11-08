---
title: "Tanzania Parliamentary Elections"
date: 2024-10-16T23:06:06-04:00
featured: true
description: "Using Python to extract constituency-level parliamentary election results from government PDFs."
tags: ["Python", "PDFPlumber"]
image: "/Tanzania/tza_adm0.png"
link: ""
fact: "Interesting little tidbit shown below image on summary and detail page"
weight: 500
sitemap:
  priority : 0.8
---

For this project, I wrote a Python script to go through government PDFs and extract individual constituency-level results of the parliamentary elections held in 2015 and 2020.

{{< figure src="/Tanzania/spotlight_councilorelections_2015_pg1.png" title="The first page of the 2015 election results PDF" >}}

{{< figure src="/Tanzania/tzelections_parliament_2020_pg1.png" title="The first page of the 2020 election results PDF" >}}


## 2015 Election Results
{{<csv-to-table "/Tanzania/tzelections_parliament2015.csv">}}

## 2020 Election Results
{{<csv-to-table "/Tanzania/tzelections_parliament2020.csv">}}
