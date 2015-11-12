## thinnercolorbar.m ##
Change colorbars thickness in groups

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/thinnercolorbar.m)

```
% thinnercolorbar Change colorbars thickness in groups
%
% [] = thinnercolorbar(CL,OPTIONS)
% 
% Change colorbars thickness in groups
%
% Inputs: 
%	CL: a list of colorbars handles
%	OPTIONS: a pair from:
%		'verticalAlignment' (string)   : 'b' (bottom) or 'm' (middle, default) or 't' (top)
%		'horizontalAlignment' (string) : 'l' (left)   or 'c' (center, default) or 'r' (right)
%		'factor' (double)
%		'offset' (double)
%			If the old colorbar thickness is L, the new one is given by:
%				L = L*factor + offset
%			By default, factor=0.9 and offset=0
%		'plothl' (handles): a list of plots (axes) handles to which correspond each of the colorbars
%			handles given by CL. This is used to ensure the function won't change the plot position.
%
%
% Created: 2010-07-07.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)