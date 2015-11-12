## nanmean.m ##
Average or mean value of matrix with NaN.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/mynanmean.m)

```
% NANMEAN Average or mean value of matrix with NaN.
%
% Y = NANMEAN(X,[DIM])
%   For vectors, NANMEAN(X) is the mean value of the elements in X. NaN
%   values are not taken account. For matrices, NANMEAN(X) is a row 
%   vector containing the mean value of each column. 
%   THIS FUNCTION IS NOW AVAILABLE ONLY FOR 2-D ARRAY !
%
%   NANMEAN(X,DIM) takes the mean along the dimension DIM of X. 
%
%   Example: If X = [0 NaN
%                    3  5]
%
%   then nanmean(X,1) is [1.5 5] and nanmean(X,2) is [0
%                                                     4]
%
%   See also MEAN, MEDIAN, STD, MIN, MAX, COV.
%
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)