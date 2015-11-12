## get\_thd.m ##
Determine the seasonal and main thermocline depths

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/get_thd.m)

```
% get_thd Determine the seasonal and main thermocline depths
%
% [THD THD_sc QC R D] = get_thd(ST,DPT,[PLOT],[DZMETHOD],[SMOOTHING])
% 
% Determine the seasonal and main thermocline depths from the vertical
% density gradient.
%
% We assume the seasonal and main thermoclines to induce two significant
% peaks in the vertical density gradient. 
% Instead of selecting the depth of the two maximums in the gradient 
% (often a useless method because of large differences in amplitude and 
% noise around the seasonal thermocline) we adopt the following method:
%
% Notation:
%	OBS: Observed profile of vertical density gradient
%	THDsc: Seasonal thermocline depth
%	THD: Main thermocline depth
%
% Method:
% 1	- THDsc is determined as the depth of the maximum in OBS (this is almost 
%		always the case).
% 2	- we create an analytical profile of reference (REF profile) for the 
%		density gradient with a gaussian of thickness 50m, centered at THDsc
%		and with the observed amplitude OBS(THDsc). We compute ER0 the
%		standard difference between REF and OBS.
% 3	- we assume the main thermocline to induce a second peak in the 
%		vertical density gradient. 
% 4	- we create another analytical profiles as the sum of REF with a second 
%		gaussian having an amplitude smaller than OBS(THDsc),
%		a larger thickness and centered at depth ZC (ANA(i) profile).
% 5	- we loop in step 4 for a range of ZC and we compute the standard difference 
%		ER(ZC) between the analytical REF+ANA(ZC) and the observed OBS 
%		vertical density gradients.
% 6	- the main thermocline depth is determined as the depth ZC for which
%		ER(ZC) is minimum.
% 7	- If ER(ZC) is found to be larger than ER0, the profile is thought to be 
%		unsignificant. Therefore we loop over steps 4, 5 and 6 with a new ANA(i) 
%		gaussian thickness until we reach a limit iteration number (QC is then 2) 
%		or found ER(ZC) smaller than the standard error ER0 (QC will be 1).
% 
%
% Inputs:
%	ST: density profile
%	DPT: vertical depth axis. Note that DPT(1) is at the surface
%		and DPT are negative defined.
% Optionals:
%	PLOT: 0 (default) or 1 
%		Plot a figure with relevant informations about the 
%		determination of depths.
%	DZMETHOD: method used to compute the vertical gradient
%		1: classic forward difference (2 points)
%		2 (default): classic centered difference (3 points)
%		3: classic centered difference (5 points)
%	SMOOTHING: 1 (default) or 0
%		This parameter determines if we should apply a little bit of
%		smoothing on the density profile before computing the vertical
%		gradient.
%	
% Outputs:
%	THD: Main thermocline depth.
%	THD_sc: Seasonal thermocline depth.
%	QC: quality flag of the estimate
%		1: reliable
%		2: why not, but weired, need a visual check
%
%	R: Standard error between all analytical and the real density profils
%	D: Depth range used to determine depth.
%
% Created: 2009-11-23.
% Rev. by Guillaume Maze on 2011-05-26: Added log method
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)