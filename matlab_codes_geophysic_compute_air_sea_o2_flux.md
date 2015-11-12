## compute\_air\_sea\_o2\_flux.m ##
Compute air-sea oxygen flux

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/compute_air_sea_o2_flux.m)

```
% compute_air_sea_o2_flux Compute air-sea oxygen flux
%
% F = compute_air_sea_o2_flux(METHOD,PARAMETERS)
% 
% Compute air-sea oxygen flux in mol/m2/s
% F is positive upward, ie for outgasing (reduction of oceanic O2)
%
% Inputs:
%	METHOD can 1 or 2:
%	METHOD = 1 : Compute the thermal component of the flux
%		as: F = -dSOL/dT * Q/Cp
%		PARAMETERS are then:
%			SST: Sea Surface Temperature in degC
%			SSS: Sea Surface Salinity in psu
%		 	Q: Air-sea heat flux (negative cooling the ocean)
%	METHOD 2 : Compute the real flux as: F = k(O2-O2sat)
%		PARAMETERS are then:
%			SST: Sea Surface Temperature in degC
%			SSS: Sea Surface Salinity in psu
%			OXY: Sea Surface Oxygen concentration in mumol/kg
%			U10: Wind speed at 10m height in m/s
%			RHO: (optional) Sea Water Density in kg/m3
%			
% Output:
%	F: air-sea oxygen flux in mol/m2/s
%
% Example:
%	SST = 25; 
%	SSS = 35.5;
%	Q   = -120;
%	F = compute_air_sea_o2_flux(1,SST,SSS,Q)
%
%	SST = 25; 
%	SSS = 35.5;
%	OXY = 280;
%	U10 = 5;
%	F = compute_air_sea_o2_flux(2,SST,SSS,OXY,U10)
%
% Created: 2010-06-28.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)