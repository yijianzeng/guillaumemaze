## gauss.m ##
Gaussian function

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/gauss.m)

```
% gauss Gaussian function
%
% y = gauss(x,sigma,x0,amp)
% 
% Give back:
%
%	y = amp*exp( -(x-x0)^2 / 2 / sigma^2 );
%
% Created: 2009-11-23 by G. Maze
% Revised: 2011-06-15 (G. Maze) Added possibility to handle multiple sigma.
% Revised: 2011-10-25 (G. Maze) Now scale input sigma by sqrt(2) so that half curve 
% 	thickness at y(x0)/exp(1) is sigma !
% Revised: 2014-04-09 (C. Feucher) Added possibility to handle multiple amplitude
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)