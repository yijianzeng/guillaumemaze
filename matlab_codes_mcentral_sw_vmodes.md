## sw\_vmodes.m ##
calculate vertical modes in a flat-bottomed ocean.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/sw_vmodes.m)

```
% SW_VMODES calculate vertical modes in a flat-bottomed ocean.
%
% [Vert,Hori,Edep,PVel]=sw_vmodes(z,N,clat,nmodes);
% Inputs:
% z is in m (higher positive the deeper you go).
% N is in rad/sec is the buoyancy frequency.  Don't pass in imaginary or
% negative buoyancy frequencies - they will be ignored.  Best done using a
% "sorted" buoyancy profile.  
% clat is a central latitude, 
% nmodes is the number of modes to calculate.
%
% Outputs: 
% Vert: Vertical velocity modes, normalized.
% Hori: Horizontal velocity modes, normalized.
% Edep: Equvalent depth of the mode in m (usefull for deformation radii)
% PVel: phase velocity of the mode in m/s.
%
% Vert and Hori are [mxn] matrices with m the length of z, and n the number
% of modes.  Edep and PVel are [1xn] matrices.
%
% CAVEAT: Solves an eigenvalue equation, which means it will create an mxm
% matrix and solve it.  Don't put in a 4000m drop with data every meter;
% smooth and decimate first!
%
% Basically solves 
%   Gzz + ev*nsq*G = 0
% subject to:
%   G(-d)=0;
%   Gz(0)-g*ev*G(0)=0
% Where G is the mode function, ev the eigenvalue, nsq the buoyancy
% frequency squared and g the gravitational constant as a fcn of latitude.
% 
% Originally written by Benno Blumenthal, 23 July 1981, in FORTRAN
% Modified for SUNS by  CC Eriksen, August 1988
% Translated to MatLab 4.2c J. Klymak, March 1997
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)