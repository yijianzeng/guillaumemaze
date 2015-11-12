## piston\_velocity.m ##
Compute a gaz air-sea interface transfer velocity (piston velocity)

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/piston_velocity.m)

```
% piston_velocity Compute a gaz air-sea interface transfer velocity (piston velocity)
%
% K = piston_velocity(GAZ,PARAMETERS)
% 
% Compute a gaz transfer velocitiy (piston velocity) for gaz GAZ.
% PARAMETERS depend on GAZ (see inputs here-after)
% 
% Inputs:
%	GAZ (string): the gaz to compute piston velocity for. In can be:
%		'OXY' for oxygen
%	PARAMETERS:
%		for GAZ = 'OXY':
%			SC: Schmidt number (see function schmidt_number)
%			U:  wind speed in m/s at 10m height
%			Here we use the Wanninkhof, 1992 formulation.
%
% Outputs:
%	K: gaz transfer velocity in m/s
%
% Created: 2010-06-28.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)