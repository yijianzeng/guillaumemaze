## project3don2d.m ##
Project a 3D field on a 2D surface

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/project3don2d.m)

```
% project3don2d Project a 3D field on a 2D surface
%
% C = projetc3don2d(Z,THREEDFIELD,TWODSURFACE)
% [Cup Cdw] = projetc3don2d(Z,THREEDFIELD,TWODSURFACE)
% [C Cup Cdw] = projetc3don2d(Z,THREEDFIELD,TWODSURFACE)
%
% Given the vertical axis Z, project the 3D variable THREEDFIELD on the
% 2D surface variable TWODSURFACE.
%
% Inputs:
%	'Z' is positive and oriented from the surface to the bottom.
%	'THREEDFIELD' is of size (NZ,N1,N2).
%	'TWODSURFACE' is of size (N1,N2) with positive values defined along 'Z'.
%
% Outputs:
%	'C' is the projected field.
%	'Cup' is the projection of the upper index.
%	'Cdw' is the projection of the lower index.
%
% Rq:
%	For any given point, the TWODSURFACE falls in between two index of the
%	Z axis (iZup and iZdw). 'Cup' and 'Cdw' are the THREEDFIELD values on 
%	these indeces and C is the linear interpolation at the TWODSURFACE level.
%
% Created: 2011-06-23.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)