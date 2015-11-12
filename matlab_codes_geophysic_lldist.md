## lldist.m ##
Compute distance in m between two points on Earth

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/lldist.m)

```
% lldist Compute distance in m between two points on Earth
%
% D = lldist(LAT,LON,[METHOD])
% 
% Compute distance in m between two points on Earth.
%
% Inputs:
%	LAT (double): Latitude (degree)
%	LON (double): Longitude (degree)
%	METHOD (optional, integer): Define the method to use:
%		1: Haversine formula
%		2: (default) Vincenty inverse formula with WGS-84 ellipsoid using mex file
%		3: Vincenty inverse formula with WGS-84 ellipsoid using Matlab routine
%
% Output:
%	D (double): distance in meters between points
%
% References:
%	T. Vincenty, Direct and inverse solutions of geodesics on the ellipsoid 
%		with applications of nested equations. 
%		Survey Review XXII, 176, April 1975
%		http://www.ngs.noaa.gov/PUBS_LIB/inverse.pdf
%
%	Vincenty formulae:  http://en.wikipedia.org/wiki/Vincenty%27s_formulae
%	Haversine formulae: http://en.wikipedia.org/wiki/Haversine_formula
%
% Created: 2009-09-30.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)