## hypsometry.m ##
Hypsometric Integral

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/hypsometry.m)

```
% HYPSOMETRY Hypsometric Integral
%
%  [i] = HYPSOMETRY(raster, classes, options, Sa, Sb);
%  PURPOSE: calculate the hypsometric integral of a raster w/ n classes and
%           plot the hypsometry curve.
%  Returns scalar [i] with hypsometric integral
% -------------------------------------------------------------------
% USAGE: [i] = hypsometry(raster, classes, plot);
% where: [raster] is the input (elevation) grid of size (cols,rows)
%        [classes] (optional) is the number of classes to use, default is
%                   total number of elements
%        [options] (optional) vector of form [1 1] specifying whether to
%                  normalize hypsometry (first element) and whether to plot
%                  curve (second element)(1=yes,0=no), default is [1 1]
%        [Sa] (optional) is a character string made from one element
%            from any or all the following 3 columns, eg 'r.':
%
%            b     blue          .     point              -     solid
%            g     green         o     circle             :     dotted
%            r     red           x     x-mark             -.    dashdot
%            c     cyan          +     plus               --    dashed
%            m     magenta       *     star             (none)  no line
%            y     yellow        s     square
%            k     black         d     diamond
%                                v     triangle (down)
%                                ^     triangle (up)
%                                <     triangle (left)
%                                >     triangle (right)
%                                p     pentagram
%                                h     hexagram
%
%        [Sb] (optional) is a vector specifying linewidth and markersize in
%        the form [lw,ms]. To set Sb, all other options have to be set as well.
% -------------------------------------------------------------------------
% OUTPUTS:
%        [i] scalar with the hypsometric integral, based on cellsize 1 and
%            number of classes. For true area, multiply with cellsize.
% -------------------------------------------------------------------
% EXAMPLE: hypsometry(abs(randn(100,100)),20,[1 1],'ro-',[2 2])
%
% NOTES: NaNs are ignored. If class numbers are provided, mean for equal
%        size classes are used for hypsometry calculation.
%
% SEE ALSO: plot, numel
%
% Felix Hebeler, Geography Dept., University Zurich, March 2007
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)