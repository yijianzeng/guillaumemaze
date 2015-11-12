## fitgauss.m ##
Fit a Gaussian to a distribution plot

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/fitgauss.m)

```
% fitgauss Fit a Gaussian to a distribution plot
%
% [H,MOM] = fitgauss([MEAN,STD])
% 
% Plot a gaussian curve on a distribution plot.
%
% Inputs:
%	MEAN, STD (optional): mean and standar deviation of the distribution
%		If not specified, they are computed from the distribution and give
%		back into output MOM
%
% Outputs:
%	H: plot handle of the gaussian curve
%	MOM = [MEAN,STD] of the distribution.
%
% Example:
%	y = randn(1,1e4);
%	hist(y,100);
%	hold on;fitgauss;
%
% Created: 2009-11-23.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)