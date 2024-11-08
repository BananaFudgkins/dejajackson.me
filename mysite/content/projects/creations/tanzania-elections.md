---
title: "Tanzania Parliamentary Elections"
date: 2024-10-16T23:06:06-04:00
featured: true
description: "Using Python to extract constituency-level parliamentary election results from government PDFs."
tags: ["Python", "PDFPlumber", "pandas"]
image: "/Tanzania/tza_adm0.png"
link: ""
fact: "Interesting little tidbit shown below image on summary and detail page"
weight: 500
sitemap:
  priority : 0.8
---

For this project, I wrote a Python script to go through government PDFs and extract individual constituency-level results of the parliamentary elections held in 2015 and 2020.

{{< figure src="/Tanzania/2015_elections_pg1.png" title="The first page of the 2015 election results PDF" >}}

{{< figure src="/Tanzania/2020_elections_pg1.png" title="The first page of the 2020 election results PDF" >}}

# Extracting the Results

I began by using the [PDFPlumber library](https://github.com/jsvine/pdfplumber) to copy all of the text in the PDF from every page that contained parliamentary election results. After extracting the raw text, I used a series of string operations to find the desired pieces of data and manipulated the text into a form that could be placed into a data table.

To separate the gathered pieces of data, I used regular expressions after identifying common symbols that could be used as delimiters to split the text.

After splitting all of the text, I stored it in custom classes. I used classes because of their ability to keep track of relationships between data. I created a class to ensure that each result would be matched with the right candidate and constituency that the election occurred in. The relationships maintained by the classes formed the basis of each row of the resulting [pandas](https://pandas.pydata.org/) dataframe.

I used the dataframe as an intermediate visualization of the extracted data to perform some intial validation of my algorithm. After I verified that the results in the dataframe matched the original contents of the PDF, I used pandas' built-in method to extract the dataframe into a CSV that can be used for further analysis by researchers or anyone interested.

# Election Results

## 2015 Results
{{<csv-to-table "/Tanzania/tzelections_parliament2015.csv">}}

## 2020 Results
{{<csv-to-table "/Tanzania/tzelections_parliament2020.csv">}}
