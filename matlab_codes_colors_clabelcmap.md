## clabelcmap.m ##
Create labels for colorbar

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/clabelcmap.m)

```
% clabelcmap Create labels for colorbar
%
% [yt ytl] = clabelcmap(hcb,cx,N,[C,F])
% 
% Create clean labels for a colorbar
% Inputs:
%	hcb: handle of the colorbar
%	cx: 2 values of the caxis
%	N:	Number of colors in the colormap
%	C = 0(default) or 1: specified if labels have to be centered on
%		each colors or placed on the edges
%	F: Indicate the format to use (default is: %0.0f)
%
% Example:
%	N = 12; cx = [-1 1]*250;
%	colormap(jet(N));
%	subplot(1,2,1);caxis(cx);cl=colorbar;clabelcmap(cl,cx,N,1);title('Labels centered');
%	subplot(1,2,2);caxis(cx);cl=colorbar;clabelcmap(cl,cx,N,0,'%g');title('Labels not centered');
%	
% Created: 2009-11-24.
% Rev. by Guillaume Maze on 2012-06-11: Added output handles
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)