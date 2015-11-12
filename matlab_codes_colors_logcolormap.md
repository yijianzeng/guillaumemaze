## logcolormap.m ##
Stretch a colormap extremum toward black and white

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/logcolormap.m)

```
% LOGCOLORMAP Stretch a colormap extremum toward black and white
%
% cmap = logcolormap(Ncol,c1,c2,cmapO,[TOPcol,BOTcol])
% Ncol is the number of points in the colormap
% [c1 c2] are the stretching parameters
% cmap0 is the initial colormap to stretch (N,3)
%
% EG:
% cmap = logcolormap(256,1,2,jet);
% % or:
% c     = [1 5];
% cx    = [-(1+2*c(1)) 1+2*c(2)];
% load mapanom
% colormap(logcolormap(256,c(1),c(2),mapanom);
% caxis(cx);
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)