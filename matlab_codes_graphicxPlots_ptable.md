## ptable.m ##
Creates non uniform subplot handles

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/ptable.m)

```
% PTABLE Creates non uniform subplot handles
%
% SUBPLOT_HANDLE = ptable(TSIZE,PCOORD)
%
% This function creates subplot handles according to
% TSIZE and PCOORD.
% TSIZE(2) is the underlying TABLE of subplots: TSIZE(1)
%	is the number of lines, TSIZE(2) the number of rows
% PCOORD(:,2) indicates the coordinates of the subplots, ie
% 	for each PCOORD(i,2), the subplot i extends from
%	initial subplot PCOORD(i,1) to subplot PCOORD(i,2)
%
% Example: 
%	figure
% 	subp = ptable([3 4],[1 6 ; 3 4 ; 9 11; 8 8]);
%	x = 0:pi/180:2*pi;
%	axes(subp(1));plot(x,cos(x));
%	axes(subp(2));plot(x,sin(x));
%	axes(subp(3));plot(x,sin(x.^2));
%	axes(subp(4));plot(x,sin(x).*cos(x));
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)