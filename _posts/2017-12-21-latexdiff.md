---
title: "Compare Latex documents with latexdiff on Mac"
excerpt: "Simple way to compare Latex documents"
tags:
  - Latex
---

Quick comparison of two Latex documents

    latexdiff ../path/old.tex new.tex --flatten > diff.tex

`--flatten` here means to unwrap all included files into a flat text

At the end the difference looks like this:
![Result](/assets/images/latexdiff.png)
