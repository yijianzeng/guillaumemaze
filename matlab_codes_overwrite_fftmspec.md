## fftmspec.m ##
Module Spectra of the Fourier Transform

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/overwrite/fftmspec.m)

```
% FFTMSPEC Module Spectra of the Fourier Transform
%
% FFTMSPEC(XT,T) Plots the signal XT versus time T and the absolute value of the the discrete 
% Fourier transform (DFT) of the signal vector XT versus the a frequency vector F.
%
% [XFM,F] = FFTMSPEC(XT,T) Returns the Fourier Transform of XT and the frequency range in
% vectors XFM and F.
%
% Considerations:
% - XT and T must be row vectors of the same length.
% - T must have an even number of elements .
% - Tn<Tn+1, Tn+1=Tn+T.
%
% The graphical output is a figure of two graphics.
% Use SUBPLOT(2,g,1) to handle the graphics.
%
% Plese send any comments to jrojasz@telcel.net.ve 
% Future comments. Jess A. Rojas Zavarce.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)