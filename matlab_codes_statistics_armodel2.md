## armodel2.m ##
Two Dimensional Spectral Estimation

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/armodel2.m)

```
% ARMODEL2 Two Dimensional Spectral Estimation
%
% [a,variance] = ARMODEL2(x,m,n,mode)
%
% Wang Xianju, April 2002
% Two Dimensional Spectral Estimation
% Note: The program is for Quater Plane Model Region Support ( Causal Support)
%
%
% This function determines the autoregressive coefficients by the
% Yule-Walker algorithm (sometimes known as the autocorrelation method).
%
% Input Parameters:
% ================
% 
%  x is the 2-D signal
%  m*n is the AR order 
%   mode = 1;           % Biased ACF estimates
%   model =0 is unbiased  =1 biased
% Output Parameters:
% =================
%
%   a -----------> AR coefficients
%   variance ----> Driving noise variance (real).
%
%-------------------------------------------------------------------------
%CC   = zeros(p,p);
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)