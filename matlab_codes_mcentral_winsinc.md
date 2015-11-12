## winsinc.m ##
Applies a windowed sinc filter

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/winsinc.m)

```
% WINSINC Applies a windowed sinc filter
%
% USAGE:
%   [xf,Rh,Fh] = winsinc(x,dt,fc,ns,win,ftype,fo)
%
% DESCRIPTION:
%   Windowed Sinc Filter.
%   This is a digital symetric non-recursive filter
%   which can be Lowpass, Highpass, or Bandpass
%   by using a windowed sinc function.
%   Non-Recursive filters are based on convolving 
%   the input series with a weight function.
%   Their advantage compared to recursive filters
%   is that they are always stable and matematically simpler.
%   Their disadvantage is that they may require a large
%   number of weights to achieve a desired response.
%
%INPUT VARIABLES:
%   x = vector
%   dt = Sampling Interval
%   fc = Cutoff frequency
%   ns = Width of filter 
%       (>>ns produces a steeper cutoff
%       but is more computationally expensive)
%       2*ns + 1 = Order of Filter, (Number of Filter Coef.)
%   win = Window Type:
%       'welch','parzen','hanning','hamming'
%       'blackman','lanczos','kaiser'
%   
%   ftype = 'low', 'high' o 'pass'
%   fo = Central Frequency (for bandpass only) 
%
%OUTPUT VARIABLES:
%   xf = filtered vector
%   Rh = Filter Response
%   Fh = Frequencies for Filter Response
%
%Copy-Left, Alejandro Sanchez, 2005
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)