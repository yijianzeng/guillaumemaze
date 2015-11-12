## getGRD.m ##
Compute horizontal gradient of a geographical field

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/getGRD.m)

```
% getGRD Compute horizontal gradient of a geographical field
%
% [dCdx dCdy] = getGRD(C,LAT,LON,[flag,grid])
%
% Compute horizontal gradient of a geographical field C(LAT,LON)
%
% OPTIONS:
%
% flag = 0: lat,lon are normal axis coordinates
% flag = 1: lat,lon specify the spacing between coordinates
%           ie,  length(LAT) = size(C,1) - 1
%           and, length(LON) = size(C,2) - 1
% grid = 0: if output fields are on the computation grid
% grid = 1: if output fields are moved backed on the input grid
%              (edges are filled with NaN)
% 
% Created 2007/07/01
% Rev. by Guillaume Maze on 2009-10-19: Change grid distance computation routine from "lldist" to my "lldist"
%
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)