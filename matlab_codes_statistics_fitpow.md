## fitpow.m ##
Power Law least-square curve fitting

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/fitpow.m)

```
% fitpow Power Law least-square curve fitting
%
% [A,B] = fitpow(x,y)
% 
% Estimate coefficients A and B so that:
%	y = A x^B
% is optimized in a least-square sense.
% 
% Inputs:
% 	x,y: two series of data points
% 
% Outputs:
%	A,B: Coefficients of the optimized power law relation between x and y.
%
% Reference:
% Weisstein, Eric W. "Least Squares Fitting--Power Law." 
% From MathWorld--A Wolfram Web Resource.
% http://mathworld.wolfram.com/LeastSquaresFittingPowerLaw.html
% 
% Created: 2013-07-25.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)