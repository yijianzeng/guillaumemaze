## getdblpeaks.m ##
Find indices corresponding to a common peak in two series

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/getdblpeaks.m)

```
% getdblpeaks Find indices corresponding to a common peak in two series
%
% ipeaks = getdblpeaks(C1,C2,N,Z,dZpeaks,dZseries)
% 
% We identify peaks of order N(1) in C1 and N(2) in C2 and then
% try to find common peaks.
%
% Inputs:
% 	C1 and C2 are two 1xn series.
%	N = [n1 n2] specify the order of each peaks. See: getpeaks
%	Z is the common axis of C1 and C2.
%	dZpeaks is the maximum distance between peaks of each series.
%		(ie, larger than dZpeaks they are merged)
%	dZseries is the minimum distance between peaks in both series.
%		(ie, larger than dZseries they are rejected)
%
% Output:
%	ipeaks is the list of indices among Z  of double peaks.
%
% Example:
%	todo !
%
% See also:
%	getpeaks
%
% Created: 2009-08-31.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)