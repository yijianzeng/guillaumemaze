## mypsdchk.m ##
Helper function for PSD, CSD, COHERE, and TFE.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/mypsdchk.m)

```
% MYPSDCHK Helper function for PSD, CSD, COHERE, and TFE.
%
%   [msg,nfft,Fs,window,noverlap,p,dflag] = MYPSDCHK(P,x,y) takes the cell 
%   array P and uses each element as an input argument.  Assumes P has 
%   between 0 and 7 elements which are the arguments to psd, csd, cohere
%   or tfe after the x (psd) or x and y (csd, cohere, tfe) arguments.
%   y is optional; if given, it is checked to match the size of x.
%   x must be a numeric vector.
%   Outputs:
%     msg - error message, [] if no error
%     nfft - fft length
%     Fs - sampling frequency
%     window - window vector
%     noverlap - overlap of sections, in samples
%     p - confidence interval, [] if none desired
%     dflag - detrending flag, 'linear' 'mean' or 'none'
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)