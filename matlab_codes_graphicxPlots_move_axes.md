## move\_axes.m ##
Move an axis (plot) within a figure

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/move_axes.m)

```
%move_axes Move an axis (plot) within a figure
%
% [] = move_axes(gc,[TYPE,PARAM])
% 
% Move the axes with handle gc according to TYPE and PARAM.
%
% TYPE:
%	'horizontalshift': Move the axis horizontally by an amount
%		given by PARAM.
%	'verticalshift': Move the axis vertically by an amount
%		given by PARAM.
%
%	'expandleft': Expand the axis toward the left by an amount
%		given by PARAM. The right axis position is preserved.
%	'setwidthleft': Change the axis width by extending/cropping it 
%		on the left side. The new width is given by PARAM.
%
%	'vshrink': Change the axis height without changing the vertical
%		position of the axis center position.
%	'hshrink': Change the axis width without changing the horizontal
%		position of the axis center position.
%
%	'reset': Set the axis back to its initial position
%
% WARNING:
%	For the 'reset' options to work nicely, please use move_axes only
%	when all figure's axes are plotted.
%
% Rev. by Guillaume Maze on 2011-03-29: Added the reset options
% Created: 2010-11-08.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)