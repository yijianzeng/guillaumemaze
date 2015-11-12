## get\_mld.m ##
Compute a mixed layer depth

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/get_mld.m)

```
% get_mld Compute a mixed layer depth
%
% H = get_mld(S,T,Z)
% 
% Compute a mixed layer depth (MLD) from vertical profiles of salinity and temperature,
% given depth of samples.
% There are many criteria out there to compute a MLD, the one used here defined MLD as:
% the first depth for which:
%		ST(T(z),S(z)) > ST(T(z=0)-0.8,S(z=0))
% 
% Inputs:
%	S: salinity (psu)
%	T: absolute temperature (degC)
%	Z: depth (m)
% Output:
%	H: mixed layer depth (m)
%
% Rq:
%	- Absolute temperature is converted to potential temperature using the CSIRO SeaWater 
%	library function 'sw_ptmp' 
%	(You can get the library at: http://www.cmar.csiro.au/datacentre/ext_docs/seawater.htm)
%	- Potential density is computed using the 'densjmd95' function
%	- We assume the vertical axis to be sorted from top (surface) to bottom.
%
% Created: 2009-11-19.
% Rev. by Guillaume Maze on 2011-05-25: Added help
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)