## updatecolorbar.m ##
Update colorbars

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/updatecolorbar.m)

```
% updatecolorbar Update colorbars
%
% [] = updatecolorbar()
% 
% Update colorbars:
%	When the colormap of a figure is changed, colorbars
%	are not updated. This function fix this !
%
% Note: the function is automatically called by 'colormap'
%
% Example:
%	figure;
%	colormap(jet(128));colorbar
%	colormap(jet(12)); 
%	disp('The colorbar is not correct, press a key to fix it with updatecolorbar ...');pause
%	updatecolorbar
%	disp('Now colorbar is correct !')
%
% Created: 2010-11-04.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)