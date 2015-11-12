## lanczos.m ##
Filtre de lanczos

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/lanczos.m)

```
% lanczos Filtre de lanczos 
%
% [y] = lanczos(x,fn,nj)
%
% y  : output filtered data
% x  : input data
% fn : the cut off frequency (any k/n between 1/n , 0.5)
% nj : (number of points in the filter-1)/2 ; transition width of the 
%      transfer function is 1/nj.
%
% The filter uses lanczos smoothing of a square box transfert function.
%
% Auteur : C. Hemon a partir source fortran Herle Mercier.
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)