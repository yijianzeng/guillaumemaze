## removeoutliers.m ##
Remove outliers from data using the Thompson Tau method.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/removeoutliers.m)

```
%REMOVEOUTLIERS   Remove outliers from data using the Thompson Tau method.
%   For vectors, REMOVEOUTLIERS(datain) removes the elements in datain that
%   are considered outliers as defined by the Thompson Tau method (replace them
%   by NaNs). This applies to any data vector greater than three elements in length, 
%   with no upper limit (other than that of the machine running the script).
%
%   Example: If datain = [1 34 35 35 33 34 37 38 35 35 36 150]
%
%   then removeoutliers(datain) will return the vector:
%       dataout = [NaN    34    35    35    33    34    37    38    35    35    36   NaN]
%
%   See also MEDIAN, STD, MIN, MAX, VAR, COV, MODE.
%   This function was written by Vince Petaccio on July 30, 2009.
% Rev. by Guillaume Maze on 2013-03-11: Changes the behavior of the function so that it replace
% outliers by NaNs instead of removing them from the input. Also removed the sorting of the 
% output and can now output the indeces of outliers.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)