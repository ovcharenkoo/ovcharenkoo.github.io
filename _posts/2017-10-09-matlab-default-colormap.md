---
title: "How to set Matlab default colormap"
excerpt: "Change default colormap in Matlab"
description: "Quick tip for changing MATLAB's default colormap from Parula to Jet or any other colormap using set(groot) command"
tags:
  - Matlab
---
Standard Matlab colormap *parula* is pretty nice, but I used to *jet* and it is tedious to add colormap(jet) everywhere manually. The simple way is to change the default colormap:

![*Parula* and *Jet* colormaps](/assets/images/parula_vs_jet.png)

    set(groot,'DefaultFigureColormap',jet)

[Source](https://www.mathworks.com/matlabcentral/answers/246461-how-can-i-get-the-default-colormap-to-be-jet-in-matlab-2014b)
