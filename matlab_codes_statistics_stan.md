## stan.m ##
Return a standardized serie

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/stan.m)

```
% stan Return a standardized serie
%
% X = stan(X,[DIM])
% 
% Return a standardized serie:
%	[X - mean(X,DIM)]/std(X,[],DIM)
% 
% Mean and std are taken along DIM (1 by default)
% 
% See also: nanstan
% 
% Created: 2012-01-30 by G. Maze
% Revised: 2013-12-20 (G. Maze) Not using nanmean/nanstd anymore, because
% 	created nanstan.m for this usage
% Revised: 2014-04-09 (C. Feucher) Added possibility to handle series with 2 dimensions.
% Revised: 2014-04-10 (G. Maze) Now handle arrays with any number of dimensions
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)