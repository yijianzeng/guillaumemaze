## wstd.m ##
Compute a weighted standard deviation

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/wstd.m)

```
% wstd Compute a weighted standard deviation
%
% S = wstd(W,X)
% 
% Compute the standard deviation of values into array X with weights W.
% 	S  = sum(W) / (v1-v2) * sum( W*(X-wmean(W,X)).^2 )
% with
%	v1 = sum(W).^2;
%	v2 = sum(W^2);
%
% See also:
%	wmean
%
% Ref:
%	http://en.wikipedia.org/wiki/Mean_square_weighted_deviation
%
% Created: 2011-02-14.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)