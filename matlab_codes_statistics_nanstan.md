## nanstan.m ##
Return a standardized serie discarding NaNs

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/nanstan.m)

```
% nanstan Return a standardized serie discarding NaNs
%
% X = nanstan(X,[DIM])
% 
% Return a standardized serie:
%	[X - nanmean(X,DIM)]/nanstd(X,[],DIM)
%
% Mean and std are taken along DIM (1 by default)
% 
% See also: nanstan
%
% Created: 2013-12-20 by G. Maze
% Revised: 2014-04-09 (C. Feucher) Added possibility to handle series with 2 dimensions.
% Revised: 2014-04-10 (G. Maze) Now handle arrays with any number of dimensions
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)