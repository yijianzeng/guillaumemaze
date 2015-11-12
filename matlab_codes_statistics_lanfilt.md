## lanfilt.m ##
High, low, band pass filters based on Lanczos filter

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/lanfilt.m)

```
% LANFILT High, low, band pass filters based on Lanczos filter
%
% Y = LANFILT(X,FILTER_TYPE,HFc,LFc,N)
% 
% Filter 1D signal X through a Lanczos filter.
%
% Inputs:
%	X: Input signal (1 dimension of length n)
%
%	FILTER_TYPE: Type of filtering you want:
%			1 : Low-pass  (cutoff frequency is LFc)
%			2 : High-pass (cutoff frequency is HFc)
%			3 : Band-pass (retain signal frequency within HFc<->LFc)
%
%	HFc: High frequency cut off (any k/n between 1/n and 1)
%	LFc: Low frequency cut off (any k/n between 1/n and 1)
%
%	N: Number of points in the filter. Note that the transition width 
%		of the transfer function is 2/(N-1)
%
% Outputs:
%	Y: Filtered signal
%
% Rev. by Guillaume Maze on 2010-02-18: Improved help, changed arguments order, add arguments check
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)