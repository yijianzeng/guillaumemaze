## getdS.m ##
Compute 2D surface elements matrix

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/getdS.m)

```
% getdS Compute 2D surface elements matrix
%
% [dS, dx, dy] = getdS(LATITUDE,LONGITUDE,[ISSYM,METHOD])
%
% Compute 2D surface elements matrix from geographical
% axis LATITUDE(northward) and LONGITUDE(eastward)
% 
% Options:
%	ISSYM = 0/1 indicates if the longitudinal axis is zonaly
%		symetric or not (by default it's not: 0)
%	METHOD = 1/2 indicates the method to use when computing
%		distances between points (see routine lldist). By
%		default it's 2.
%
% Created: 2009-09-14.
% Rev. by Guillaume Maze on 2009-09-30: Added dx,dy optional output
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)