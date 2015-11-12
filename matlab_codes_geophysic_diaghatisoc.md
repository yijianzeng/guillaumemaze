## diagHatisoC.m ##
Compute iso-surface of a 3D field

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/diagHatisoC.m)

```
% diagHatisoC Compute iso-surface of a 3D field
%
% [H,[dH,h,dh]] = diagHatisoC(C,Z,isoC,[dC])
%
% Given the 3D field C(depth,lat,lon) and the vertical
% axis Z(<0,downward), this function computes the 2D 
% iso-surface such like C(H or h) = isoC
% Eventualy computes a thickness with parameter dC.
%
% OUTPUTS:
% H(lat,lon)  is the depth determined with the input resolution
% dH(lat,lon) is the thickness of the layer: isoC-dC < C < isoC+dC from H
% h(lat,lon) is a more accurate depth (determined with interpolation)
% dh(lat,lon) is the interpolated thickness of the layer: isoC-dC < C < isoC+dC from h
%
% Created: 2007-06.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)