## trend.m ##
Find a linear trend from a vector, usually for FFT processing.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/trend.m)

```
% TREND Find a linear trend from a vector, usually for FFT processing.
%   Y = TREND(X) finds the best straight-line fit linear trend from 
%   the data in vector X and returns it in vector Y.  If X is a matrix,
%   TREND finds the trend from each column of the matrix.
%
%   Y = TREND(X,'constant') finds just the mean value from the vector X,
%   or the mean value from each column, if X is a matrix.
%
%   Y = TREND(X,'linear',BP) finds a continuous, piecewise linear trend.
%   Breakpoint indices for the linear trend are contained in the vector BP.
%   The default is no breakpoints, such that one single straight line is
%   removed from each column of X.
%
%   See also DETREND, MEAN
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)