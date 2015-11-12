## floatAxisY\_right.m ##
floatAxisY create floating x-axis for multi-parameter plot

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/floatAxisY_right.m)

```
% floatAxisY  create floating x-axis for multi-parameter plot
% =========================================================================
% floatAxisY  Version 1.2 6-Mar-2000
%
% Usage: 
%   [h1,ax2,ax3] = floatAxisY(varargin)
%
% Description:
%   This Matlab function creates a floating y-axis for mutli-parameter
%   plots with different units on the same figure. For example, in oceanography,
%   it is common to plot temperature, salinity, and density versus depth.
%
%
% Input:
%   A minimum of two parameters is required. 
%	The first and second parameters are the x,y pairs to plot. 
%	The third parameter (optional) specifies the linestyle
%		(defaults to 'k-' solid black). 
%	The fourth parameter (optional) specifies the y-axis label for the floating axis. 
%	The fifth parameter (optional) specifies the x and y limits for the axis 
%		(this should be of the form [xlower xupper ylower yupper]).
%   The sixth parameter (optional) specifies the tag of axes to identify the subplot.
%		When using subplots in a figure, just add a tag to the axes and specify it
%		here. New axes will automatically have the tag inserted.
%
% Output:
%   n/a
%
% Called by:
%   CTDplotY.m - script to demo floatAxis function
%
% Calls:
%   n/a
%
% Rev. by Guillaume Maze on 2010-11-05: Add subplot management
% Rev. by Guillaume Maze on 2010-11-03: Modified to work with my Matlab
% Author:
%   Blair Greenan
%   Bedford Institute of Oceanography
%   18-May-1999
%   Matlab 5.2.1
%   greenanb@mar.dfo-mpo.gc.ca
% =========================================================================
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)