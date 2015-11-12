## load\_climOCCA.m ##
Load any climatological fields from OCCA

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/load_climOCCA.m)

```
% LOAD_CLIMOCCA Load any climatological fields from OCCA
%
% [FIELD1, FIELD2, ...] = load_climOCCA('FIELD1;FIELD2;...',MONTHS)
%
% MONTHS can be 1 to 12 of a subset like: [1:3]
% It may also be simply: 'y', 'year', 'annual' to mean MONTHS=[1:12];
% 
% EG:
% [SST,SSH,U] = load_climOCCA('sst;ssh;u',3);
% Will give back the March climatology of SST, SSH and Zonal Velocity
%
%
% Created by Guillaume Maze on 2008-10-14.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)