## diag\_interpallREQ.m ##
NEWFIELD = diag\_interpallREQ(FIELD,LON,LAT,netcdf\_domain,resolution,...

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/diag_interpallREQ.m)

```
% NEWFIELD = diag_interpallREQ(FIELD,LON,LAT,netcdf_domain,resolution,...
%                              [grid])
%
% We interpolate linearly FIELD(LAT,LON) on a grid, independant of the dataset
% with a resolution on the domain netcdf_domain.
%
% [grid] = 'T' or 'U' or 'V'
% Indicate where the field is on the C-grid
% Default is 'T'
%
% Output is:
% [NEWFIELD,LON,LAT,DLON,DLAT]
%
% 2008/02/13
% gmaze@mit.edu
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)