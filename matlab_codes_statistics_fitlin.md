## fitlin.m ##
Linear least-square curve fitting

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/fitlin.m)

```
% fitlin Linear least-square curve fitting
%
% [a,b,a_er,b_er,Rsq,Qmin] = fitlin(x,y)
% 
% Estimate a and b from the linear equation:
% 	f(x) = a + b * x
% so that the error function 
%	Q = sum( [f(x) - y]^2 )
% is minimized and thus y ~ f(x).
% 
% Inputs:
% 	x,y: two series of data points
% 
% Outputs:
%	a,b: Coefficients of the optimized linear relation between x and y.
% 	a_er, b_er: Standard errors estimates on a and b.
% 	Rsq: Square of the correlation coefficient between x and y. It is 
% 		equal to the fraction of variance explained by a the linear 
% 		least-squares fit between two variables.
% 	Qmin: Value of the error function for the best fit.
% 
% Notes:
% - If x and y are standardized (ie with zero mean and std of 1),
% then a = 0, and b = R, the correlation coefficient between x and y.
% - The coefficient 'b' is just the covariance of x with y divided by 
% the variance of x.
% 
% References:
% Weisstein, Eric W. "Least Squares Fitting." 
% From MathWorld--A Wolfram Web Resource
% http://mathworld.wolfram.com/LeastSquaresFitting.html
% See Also:
% Dennis L. Hartmann, 2002: Objective analysis (Course Notes)
%
% Created: 2013-07-23.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)