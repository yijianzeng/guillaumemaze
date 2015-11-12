## sinefit.m ##
params = sinefit(yin,t,f)

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/sinefit.m)

```
% params = sinefit(yin,t,f)
% [params,yest] = sinefit(yin,t,f)
% [params,yest] = sinefit(yin,t,f,verbose)
% [params,yest] = sinefit(yin,t,f,verbose,plotflag)
% [params,yest] = sinefit(yin,t,f,verbose,plotflag,searchflag)
% [params,yest,yres] = sinefit(yin,t,...)
% [params,yest,yres,rmserr] = sinefit(yin,t,...)
% 
% Least squares sinusoid fit - optimization toolbox not needed
%
% IEEE Standard for Digitizing Waveform Recorders (IEEE Std 1057):
% Algorithm for three-parameter (known frequency) and four-parameter 
% (general use) least squares fit to sinewave data using matrix operations.
%
% INPUTS:   -yin:        Input signal to be fitted (a vector)
%           -t:          Time vector (same length as yin)
%           -f:          Signal frequency (actual or estimate) [Hz]
%           -verbose:    if 1, display information; else, don't. default: 1
%           -plotflag:   If 1, plot; else, don't. default: 1
%           -searchflag: If 0, iterative search skipped, just fit.
%                        A quick choice you may want to try...
%                        By default searchflag = 1.
%
% -The time vector is not necessarily linearly spaced (hence required here)
% -If f is a guess, it has to be near true input signal frequency
%
% OUTPUTS:  -params:  A vector containing:
%                     [offset amplitude freq(Hz) angle(rad)].
%                     If not converged, params = [nan nan nan nan]
%           -yest:    Estimated sinusoid:
%                     offset+amplitude*cos(2*pi*frequency_Hz*t+angle_rad)
%           -yres:    The residual
%           -rmserr:  Root mean square of the residual
%
% For further information, consult IEEE Std 1057 and/or 
% IEEE Std 1241 documentation.
% 
% type sinefit for demo
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)