## scalprod.m ##
Cross or dot product of two 3D scalar fields

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/scalprod.m)

```
% scalprod Cross or dot product of two 3D scalar fields
%
% [a1,a2,a3] = scalprod(DZ,DY,DX,A,B,WPROD)
% 
% Compute either the cross or dot products of the two
% scalar fields A and B.
% A and B are of dimensions: (NZ,NY,NX)
% DX,DY,DZ are distances between A,B grid points
% 	DX: DX(NZ,NY,NX-1)
% 	DY: DY(NZ,NY-1,NX)
% 	DZ: DZ(NZ-1,NY,NX)
%
% WPROD is 1 or 'x' for the cross product
% then:
% 	Jx =   d(A)/dy.*d(B)/dz - d(A)/dz.*d(B)/dy;
% 	Jy = -(d(A)/dx.*d(B)/dz - d(A)/dz.*d(B)/dx);
% 	Jz =   d(A)/dx.*d(B)/dy - d(A)/dy.*d(B)/dx;
%
% WPROD is 2 or '.' for the dot product
% then:
% 	Jx =   d(A)/dx.*d(B)/dx
% 	Jy =   d(A)/dy.*d(B)/dy
% 	Jz =   d(A)/dz.*d(B)/dz
%
% Vector components a1,a2 and a3 are given back on the 
% same grid as A and B.
% Outputs depend on the number of fields asked and on WPROD:
% For WPROD a CROSS PRODUCT:
% 	a1 only		: a1=Jz, ie the curl
% 	a1,a2 only	: a1=Jy, a2=Jx
% 	a1,a2,a3	: a1=Jz, a2=Jy, a3=Jx
% For WPROD a DOT PRODUCT:
% 	a1 only		: a1=Jx+Jy+Jz
% 	a1,a2 only	: a1=Jy, a2=Jx
% 	a1,a2,a3	: a1=Jz, a2=Jy, a3=Jx
%
% Created: 2008-12-14.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)