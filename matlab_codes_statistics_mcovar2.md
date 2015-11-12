## mcovar2.m ##
Two Dimensioal Spectral Estimation

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/mcovar2.m)

```
% MCOVAR2 Two Dimensioal Spectral Estimation
%
% Wang Xianju
% Two Dimensioal Spectral Estimation
% Convariance Method and Modified Convariance Method
% This function implements the modified covariance method for estimation
% of the AR parameters.
%
% [a,variance]=mcovar2(x,m,n,mode)
% Input Parameters:
% ================
%
%   x -----------> two dimensional data 
%   m*n -----------> Order of autoregressive process
%   mode =1  modified Convariance Method
%   mode =0  Convariance Method
% Output Parameters:
% =================
%
%   a -----------> AR coefficients, a(0,0), a(0,1),.......
%   variance ----> Driving noise variance (real)
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)