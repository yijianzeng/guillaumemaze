## ploterr.m ##
General error bar plot.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/ploterr.m)

```
%PLOTERR General error bar plot.
%
%
% Usage for the impatient
% =======================
%
%  X, Y: x and y axis values
%  xerr, yerr: if matrix relative error
%              if cell array lower and upper bound
%  LineSpec as in plot. If passed it must be between yerr and properties.
%  Properties: 'logx', 'logy', 'logxy':
%                 toggles for logarithmic scaling, no value needed
%              'hhx', 'hhy', 'hhxy':
%                 relative handle sizes (Handle Height)
%              'abshhx', 'abshhy', 'abshhxy':
%                 absolute handle sizes. Total height for linear scale,
%                 fraction of power of 10 for log scale.
%
%  X, Y, xerr and yerr must be of the same size as long as dimensions are
%  not equal to 1, otherwise singletons are expanded. You can pass every-
%  thing you like, e.g. xerr={0, 20:29} and x=[(1:10)' (2:11)'] to
%  indicate a lower bound of 0 for all values and an upper bound of 20:29
%  for both columns of x, which will show up as two separate lines.
%
%
% USAGE
% =====
%
%   PLOTERR(X,Y,EX,EY) plots X vs. Y with x error bars [X-XE X+XE] and y
%   error bars [Y-YE Y+YE].
%
%   PLOTERR(X,Y,{LX,UX},{LY,UY}) plots the graph of vector X vs. vector Y
%   with error bars specified by LX and UX in horizontal direction and
%   with error bars specified by LY and UY in vertical direction.
%   L and U contain the lower and upper error ranges for each point
%   in X resp. Y (L = lower, U = upper).  Each error bar ranges from L(i)
%   to U(i). X, LX and UX sizes may vary in singleton dimensions only, the
%   same accounts for Y, LY and UY. If any of X,Y,LX,UX,LY,UY is a matrix
%   then each column produces a separate line.
%
%   PLOTERR(X,Y,[],EY) plots no x error bars
%   PLOTERR(X,Y,EX,[]) plots no y error bars
%   PLOTERR(X,Y,EX,{LY,UY}) plots x errors [X-XE X+XE] and y errors [LY UY]
%   ... etc ...
%
%   PLOTERR(X,Y,EX,EY,LineSpec) uses the color and linestyle specified by
%   the string LineSpec. See PLOT for possibilities. Defaults to a solid
%   line connecting the points (X,Y).
%
%   PLOTERR(X,Y,EX,EY,LineSpec,'Property1',Value1,'Property2',Value2,...)
%   Property Value pairs can be passed after LineSpec, however, LineSpec
%   does not need to be passed.
%   The Following properties are available:
%   - 'logx', 'logy', 'logxy': Logarithmic scaling of x axis, y axis or
%    both. A value is not required. If you still specify a value, 0 turns
%    log scale off, 1 turns it on. E.g. PLOTERR(X,Y,EX,EY,'logx') plots on
%    a logarithmically scaled x axis.
%   - 'hhx', 'hhy', 'hhxy': relative size of bar handles compared to the
%    average distance of the datapoints. The default for hhx and hhy is
%    2/3, indicating a total width of the bar handles of 2/3 of the mean
%    distance of datapoints in y. For logarithmic plots that is the mean
%    distance on a logarithmic scale.
%    E.g. PLOTERR(X,Y,EX,EY,'logy','hhy',0.1) plots normal x error bars and
%    tiny y errorbars on a logarithmic y scale and a linear x scale.
%   - 'abshhx', 'abshhy', 'abshhxy': absolute size of bar handles for
%    linear scale, absolute size in units power of 10 for logscale, i.e.
%    the command PLOTERR(...,'logy','abshhx',1.0) produces x handlebars
%    spanning each one decade on the y axis.
%   
%   H = PLOTERR(...) returns a vector of line handles in the order:
%      H(1) = handle to datapoints
%      H(2) = handle to errorbar y OR errorbar x if error y not specified
%      H(3) = handle to errorbar x if error y specified
%   If more than one line is plotted, the ordering is the following:
%      H(1:n) = handle to lines with datapoints
%      H(n+1:2*n) = handle to y error bars
%      H(2*n+1:3*n) = handle to x error bars
%
%   NOTES:
%   ------
%    - If both abshh* and hh* are set, the latter of both in the argument
%      list is used. The same is true for any of the other properties
%      passed twice.
%    - Properties ending on 'xy' may also end on 'yx' or you can leave the
%      ending away: logxy = logyx = log
%    - You cannot pass PLOT properties like 'LineWidth'. To use those
%      plot properties, call set(h(i),'Property',Value) with i according
%      to the specification for H = PLOTERR(...) above.
%
%
% Examples
% ========
%
%   Basic example:
%   -------------
%
%      x = 2:11;
%      y = sin(x);
%      e = std(y)*ones(size(x));
%      ploterr(x,y,e)
%
%   Draws symmetric error bars of unit standard deviation along a sine wave.
%
%   
%   Extended example:
%   -----------------
%
%      x = 0:15;
%      y=exp(-x).*(rand(1,16)*0.9+0.1);
%      h=ploterr(x,y,0.3,{exp(-x)*0.1 exp(-x)},'r.','logy','hhxy',0.5)
%      set(h(2),'Color','b'), set(h(3),'Color','b')
%      legend(h,{'data' 'error x' 'error y'})
%
%   Draws samples of a noisy exponential function on a logarithmic y scale
%   with constant relative errors in x and variable absolute errors in y with
%   slim error bar handles. The lineseries objects are used to set the color
%   of the error bars and to display a legend.
%
%
% Acknowledgements
% ================
%
%  technique for plotting error bars
%  ---------------------------------
%   L. Shure 5-17-88, 10-1-91 B.A. Jones 4-5-93
%   $Revision: 5.19 $  $Date: 2002/06/05 20:05:14 $
%
%  modified for plotting horizontal error bars
%  -------------------------------------------
%   Goetz Huesken
%   e-mail: goetz.huesken(at)gmx.de
%   Date: 10/23/2006
%
%
% Version History
% ===============
%  
%  v1.0, October 2008: modification of errorbar_x by Goetz Huesken for
%          plotting horizontal and/or vertical errorbars and to support
%          logarithmic scaling.
%  v1.1, December 2008: changed the user interface. Handle sizes and
%          logarithmic scaling can now be set via properties. LineSpec is
%          not compulsory anymore when setting logscale or handle sizes.
%  v1.1.1, December 2008: bugfix of v1.1
%  v1.1.2, February 2009: added abshh properties to set handle sizes as
%          absolute values
%
%   Felix Zrgiebel
%   email: felix_z -> web.de
%   Date: 12/03/2008
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)