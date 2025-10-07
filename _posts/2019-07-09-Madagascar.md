---
title: "Useful commands for data processing in Madagascar"
excerpt: "Disconnected code snippets"
description: "Quick reference guide for Madagascar seismic processing software - commands for reading SEGY files, plotting RSF data, and windowing operations"
tags:
  - Madagascar
---

## Segy to RSF

    sfsegyread < file.sgy > file.rsf

## Plot from .rsf
    sfgrey < file.rsf | sfpen
if complex, pipe ```| sfreal | sfpen```

## Brief about the .rsf
    sfin < file.rsf

## Crop window from .rsf
     sfwindow < file.rsf n1=2000 n2=500 > file2.rsf

```Example: sfwindow < file.rsf n1=2000 n2=500 | sfgrey | sfpen```