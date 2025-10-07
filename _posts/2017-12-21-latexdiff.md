---
title: "Compare Latex documents with latexdiff on Mac"
excerpt: "Simple way to compare Latex documents"
description: "Quick guide to using latexdiff command-line tool on Mac for comparing and highlighting differences between LaTeX document versions"
tags:
  - Latex
---

Quick comparison of two Latex documents

    latexdiff ../path/old.tex new.tex --flatten > diff.tex

`--flatten` here means to unwrap all included files into a flat text

At the end the difference looks like this:
![Result](/assets/images/latexdiff.png)

Beware that sometimes the resulting `diff.tex` file is compiled with errors. Usually they are resolved by removing preceeding the error empty lines or adding `$` arround math symbols.
