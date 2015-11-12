## bin1mat.m ##
create a 1D matrix from scattered data without interpolation

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/bin1mat.m)

```
% bin1mat create a 1D matrix from scattered data without interpolation
%
%   YG = BIN1MAT(X,Y,XI) - creates a grid from the data 
%   in the (usually) nonuniformily-spaced vectors (x,y) 
%   using grid-cell averaging (no interpolation). The grid 
%   dimensions are specified by the uniformily spaced vectors
%   XI.
%
%   YG = BIN1MAT(...,@FUN) - evaluates the function FUN for each
%   cell in the specified grid (rather than using the default
%   function, mean). If the function FUN returns non-scalar output, 
%   the output YG will be a cell array.
%
%   YG = BIN1MAT(...,@FUN,ARG1,ARG2,...) provides aditional
%   arguments which are passed to the function FUN. 
%
% This function is 1D version of the bin2mat function from A. Stevens (astevens@usgs.gov)
% available on Matlab Central.
% 
% Created: 2013-05-13.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)