---
title: "Transparent background when saving figures in Matlab (e.g png, eps etc.)"
tags:
  - Matlab
---

Often you need to generate multiple figures with transparent background in order to put them directly into TeX document or presentation, but Matlab is prone to saving with white background using `print` 

## Problem:
![Transparent vs non-transparent  background](/assets/images/transparent_background.png)

## Solution:
Use [export_fig](http://www.mathworks.com/matlabcentral/fileexchange/23629-export-fig) by Yair Altman. 

"This function saves a figure or single axes to one or more vector and/or bitmap file formats, and/or outputs a rasterized version to the workspace, with the following properties

- Figure/axes reproduced as it appears on screen 
- Cropped/padded borders (optional) 
- Embedded fonts (pdf only) 
- Improved line and grid line styles 
- Anti-aliased graphics (bitmap formats) 
- Render images at native resolution (optional for bitmap formats) 
- Transparent background supported (pdf, eps, png, tiff) 
- Semi-transparent patch objects supported (png, tiff) 
- RGB, CMYK or grayscale output (CMYK only with pdf, eps, tiff) 
- Variable image compression, including lossless (pdf, eps, jpg) 
- Optional rounded line-caps (pdf, eps) 
- Optionally append to file (pdf, tiff) 
- Vector formats: pdf, eps 
- Bitmap formats: png, tiff, jpg, bmp, export to workspace"

## HOW TO

1. Download the package from [here](http://www.mathworks.com/matlabcentral/fileexchange/23629-export-fig) (sign in if required)
2. Unzip it and place to the folder with your project (rename it if needed e.g. to *export_fig_folder*)
3. Add the folder to path by *Right Click -> Add to path -> Selected folders and subfolders*, or by adding `addpath('./export_fig_folder/')` to your script

Use function in the following manner:

Add `set(gcf, 'Color', 'None')` to your figure property or `-transparent` key when calling function  

    save_path = '../pics/MyPic';
    export_fig(save_path,'-png','-eps');

or:

    export_fig ../pics/MyPic -png -eps;

