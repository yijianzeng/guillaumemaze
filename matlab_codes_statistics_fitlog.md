## fitlog.m ##
Logarithmic least-square curve fitting

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/fitlog.m)

```
% fitlog Logarithmic least-square curve fitting
%
% [a,b] = fitlog(x,y)
% 
% Estimate coefficients a and b so that:
%	y = a + b*log(x)
% is optimized in a least-square sense.
% 
% Inputs:
% 	x,y: two series of data points
% 
% Outputs:
%	a,b: Coefficients of the optimized logarithmic relation between x and y.
%
% Reference:
% Weisstein, Eric W. "Least Squares Fitting--Logarithmic." 
% From MathWorld--A Wolfram Web Resource. 
% http://mathworld.wolfram.com/LeastSquaresFittingLogarithmic.html
% 
% Created: 2013-07-25.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)