## getpeaks.m ##
Determine peak(s) of function X

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/getpeaks.m)

```
% getpeaks Determine peak(s) of function X
%
% ipeaks = getpeaks(X,[N])
%
% Determine peaks of function X. N is the 'order' of the peak selection
% criteria (By default, N=2). The 'order' of the peak indicates the number 
% of points on each side of the peak to which X(ipeaks) is superior to:
% X(ipeak) is the maximum in the interval: X(ipeak-N:ipeak+N)
%
% Example:
%
% See also:
%	getdblkpeaks
%
% Created: 2007.
% Rev. by Guillaume Maze on 2009-08-31: Fix a bug with find
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)