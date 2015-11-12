## refline.m ##
Add a reference line to a plot.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/overwrite/refline.m)

```
% REFLINE Add a reference line to a plot.
%   REFLINE(SLOPE,INTERCEPT,[LINE_OPTIONS]) adds a line with the given SLOPE and
%   INTERCEPT to the current figure.
%
%   REFLINE(SLOPE) where SLOPE is a two element vector adds the line
%        y = SLOPE(2) + SLOPE(1)*x 
%   to the figure. (See POLYFIT.)
%
%   H = REFLINE(SLOPE,INTERCEPT,[LINE_OPTIONS]) returns the handle to the line object
%   in H.
%
%   REFLINE with no input arguments superimposes the least squares line on 
%   the plot based on points recognized by LSLINE.
%
%   See also POLYFIT, POLYVAL, LSLINE. 
%
% Rev. by Guillaume Maze on 2011-02-10: Add tag 'refline' to the line
% Rev. by Guillaume Maze on 2011-02-10: Add line options
%	LINE_OPTIONS: Any options pair to a line object
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)