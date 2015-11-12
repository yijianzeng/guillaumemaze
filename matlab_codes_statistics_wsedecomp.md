## WSEdecomp.m ##
Split a signal into its downward/upward propagating and stationnary components

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/WSEdecomp.m)

```
% WSEDECOMP Split a signal into its downward/upward propagating and stationnary components
%
% [Sf A FX FT] = WSEdecomp(S,DT,DX,[PERIOD],[WAVELENGTH]) 
% Split S(SPACE,TIME) into: DW/ST/UP-waves
%
% Split the signal S(SPACE,TIME) into its downward/upward space 
% propagating and stationnary components via a 2D Fourier decomposition.
% S is a (SPACE,TIME) matrix. We eventually proceed to a space and/or 
% time filtering. DT,DX are temporal and space step. PERIOD=[Tmin Tmax] 
% and WAVELENGTH=[Xmin Xmax] are time and space band-pass filters 
% specifications.
%
% Sf(DIRspec,SPACE,TIME) are each components with:
%    DIRspec=1 -> Downward part (decreasing space axis)
%    DIRspec=2 -> Stationnary part
%    DIRspec=3 -> Upward part (increasing space axis)
%
% A(DIRspec,SPACE/2,TIME/2) are propagative Power Spectral Density with:
%    DIRspec=1 -> Downward part (decreasing space axis)
%    DIRspec=2 -> Upward part (increasing space axis)
% Rq: SPACE and TIME must be even
%
% FX and FT are space and time wavenumbers:
%    FX -> Space wavenumber, ie: 2*pi*[0:SPACE/2-1]/DX/SPACE
%    FT -> Time wavenumber, ie: 2*pi*[0:TIME/2-1]/DT/TIME
% 
% PERIOD=[Tmin Tmax] is in real time axis unit
% WAVELENGTH=[Xmin Xmax] is in real space axis unit
%
% Rq: 
%   - PERIOD/WAVELENGTH=[0 Inf] produce no filtering
%   - Tmin or Xmin = 0   will produce high-pass filtering
%   - Tmax or Xmax = Inf will produce low-pass filtering
%
% Ref: Park et al (2004) GRL V31
%      Park (1990) C. R. Acad. Sci. Paris 310(II) p919-926
%      J. Le Sommer, personnal communication
%================================================================
%
%  Guillaume MAZE
%  Last reviewed:
%                 Nathalie Daniault - September 2004
%                 -> Vectorisation of recomposition loop
%                 Nathalie Daniault - August 2004
%                 -> Change phases definition and 
%                    adapt to a signal with non nul mean
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)