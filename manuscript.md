---
title: "Command line tools for a simpler markdown experience"
author:
- institute: Brain and Mind Institiute, University of Western Ontario
  name: Naveed Ejaz
abstract: This document demonstrates a pipeline from going from a markdown document
  to nicely formatted pdf or html documents. Typically, a markdown user would have to understand third party tools like pandoc which offer ways of converting from markdown to pdf/html. This can be daunting for novice users, Therefore, I have provided a set of command line tools that makes the process of providing input to the pandoc compiler as simple as executing a single line. The command line tools handle everything from linking the bibliography file to providing default templates for formatting the desired output files. Templates are provided for compiling markdown files directly to html using a cascade style-sheet, and for converting markdown to pdf indirectly by first compiling to latex and then to pdf. Experience users will be able to modify the command line tools and the templates that accompany this tutorial to finely control the output files. Further details are provided in the make_pdf and make_html command line tools. Hopefully, these command line tools and templates help make the whole markdown process very simple for you!
---

# Introduction

Markdown offers a way of writing academic papers by separating the actual text from the formatting of the manuscript. It is fast, and simple to learn. Since it works on plain text files, it can be used with github, gitlab or bitbucket for version control. This makes it a very powerful tool for open-science. 

In this tutorial, we will go over a few basics of how to use markdown to compile plain text into formatted manuscripts that can be shared with colleagues. This tutorial is not meant to provide a complete overview of markdown, but rather make it easy for you to go from a plain text markdown file to a formatted pdf or html output.

## Setting up pandoc to convert markdown to pdf/html

This tutorial requires that pandoc is correctly installed on the current machine. The easiest way to get it on a mac is to open a terminal window, and use the brew project dependency manager to install the pandoc. To do this, open up a terminal window, and type the following commands: `brew install pandoc pandoc-citeproc pandoc-crossref`.

## Quick introduction to markdown

Once you have pandoc all setup, lets take a look at what options markdown has to offer: 

We can make either number lists,

1. Superscripts and subscripts can be inserted as x^i^ or x~i~  
2. Equations can be inserted in-line using $y_x$, or alternatively they can be inserted as an array:

$$ y = t_i + x_i  $$

## Citations with markdown

Markdown and pandoc offers a quick and easy way to add citations to your manuscript. All you need is a bibliography in bibtex format, and then the citation can be added to the document using the  `[@cite_key]` notation. For example, a citation can be inserted in full like this [@Ejaz:2017fo], or alternatively the author can be suppressed like by using the minus notation `[-@cite_key]` like this [-@Diedrichsen:2017fy].

## Images and hyper-links

Markdown also offers an easy way to insert hyper-links into your document (example: [Google](http://www.google.com)), as well as inserting images with typeset captions.  

![Figures and captions are nicely typeset in markdown](img.jpg)

## Generating pdf and html files

To make going from markdowns plan files to nicely formatted pdf and html requires understanding the details of how pandoc works. For most, this can be a big hassle. Therefore, I have provided you with two scripts alongside this template which makes the whole process as simple as running one command. To generate pdf files, open a terminal window, and navigate to the directory with this file, and execute the command `./make_pdf` to generate pdf files and `./make_html` to generate html files, respectively.

# References

