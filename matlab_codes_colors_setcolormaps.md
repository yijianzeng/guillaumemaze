## setcolormaps.m ##
Sets the colormap as the union of two at certain level.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/setcolormaps.m)

```
% SETCOLORMAPS Sets the colormap as the union of two at certain level. 
%
%   SETCOLORMAPS(MAPINF,MAPSUP,Z0) sets the colormap of the current figure 
%   with the colormap MAPINF from the bottom to Z0 and MAPSUP from Z0 to 
%   the top of the surface, where the first two entries are the names of 
%   the colormaps (strings). To get a reverse colormap put '-1' at the end
%   of his name. 
%   
%   SETCOLORMAPS(MAPINF,MAPSUP,[Z0 DZ]) each band of DZ high from the Z0 
%   level are colored with different color.
%
%   SETCOLORMAPS(MAPINF,MAPSUP,Z0,N), where N is integer, sets a colormap
%   with N different colors. Default N=256. It's ignored when DZ is used.
%
%   Note: the caxis are changed in order to split the colormap exactly at
%   Z0.
%
%   Example:
%      figure(1)
%      surf(peaks) 
%      setcolormaps('copper','summer-1',2.5)
%       shading interp, colorbar, axis tight, zlabel('Metros')
%       title('Union at 2.5 m')
% 
%      figure(2)
%      surf(peaks) 
%      setcolormaps('copper','summer-1',[2.5 0.5])
%       shading interp, colorbar, axis tight, zlabel('Metros')
%       title('Union at 2.5 m and different color for each 0.5 m band')
% 
%      figure(3)
%      surf(peaks) 
%      setcolormaps('copper','summer',2.5,10)
%       shading interp, colorbar, axis tight, zlabel('Metros')
%       title('Union at 2.5 m with 10 colors')
%  
%   See also COLORMAPEDITOR, COLORMAP, CAXIS
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)