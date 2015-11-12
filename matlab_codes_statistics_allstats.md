## allstats.m ##
STATM Compute statistics from 2 series

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/allstats.m)

```
% STATM Compute statistics from 2 series
%
% STATM = allstats(Cr,Cf)
%
% Compute statistics from 2 series considering Cr as the reference.
% 
% Inputs:
%	Cr and Cf are of same length and uni-dimensional. They may contain NaNs.
%
% Outputs:
% 	STATM(1,:) => Mean
% 	STATM(2,:) => Standard Deviation (scaled by N)
% 	STATM(3,:) => Centered Root Mean Square Difference (scaled by N)
% 	STATM(4,:) => Correlation
%
% Notes:
%	- N is the number of points where BOTH Cr and Cf are defined
%
% 	- NaN are handled in the following way: because this function
% 		aims to compair 2 series, statistics are computed with indices
%		where both Cr and Cf are defined.
%
% 	- STATM(:,1) are from Cr (ie with C=Cr hereafter)
% 	  STATM(:,2) are from Cf versus Cr (ie with C=Cf hereafter)
%
%	- The MEAN is computed using the Matlab mean function.
%
%	- The STANDARD DEVIATION is computed as:
%			          /  sum[ {C-mean(C)} .^2]  \
%			STD = sqrt|  ---------------------  |
%			          \          N              /
%
%	- The CENTERED ROOT MEAN SQUARE DIFFERENCE is computed as:
%			           /  sum[  { [C-mean(C)] - [Cr-mean(Cr)] }.^2  ]  \
%			RMSD = sqrt|  -------------------------------------------  |
%			           \                      N                        /
%
%	- The CORRELATION is computed as:
%			      sum( [C-mean(C)].*[Cr-mean(Cr)] ) 
%			COR = --------------------------------- 
%			              N*STD(C)*STD(Cr)
%
%	- STATM(3,1) = 0 and STATM(4,1) = 1 by definition !
%
% Created by Guillaume Maze on 2008-10-28.
% Rev. by Guillaume Maze on 2010-02-10: Add NaN values handling, some checking
%				in the inputs and a more complete help
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)