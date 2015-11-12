## ahline.m ##
Draw a horizontal line on a plot and print value on the y-axis

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/ahline.m)

```
% ahline Draw a horizontal line on a plot and print value on the y-axis
%
% [h,t] = ahline([Y,STYLE])
% 
% Draw a horizontal line on a plot and print value on the y-axis.
% Style apply to both the line and the text.
%
% Inputs:
%	Y: intersection of the line with the y-axis
%		By default it is set to: y=0
% 	STYLE: is any pair of properties for a line and/or text object.
%		Default is plain black. 
%
% Outputs:
%	h: line handle
%	t: text handle
% 
% Example:
%	ahline(3,'color','r')
%	ahline(3,'color','r','linewidth',12,'fontsize',20,'linestyle','--')
%
% See also:
%	hline, vline, refline
%
% Created: 2011-03-08.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)