## colormap\_cpt.m ##
builds a matlab colormap from a cpt file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/colormap_cpt.m)

```
% COLORMAP_CPT   builds a matlab colormap from a cpt file 
%
%    colormap_cpt(name,<nSteps>)
%
% name   = the name of a colormap from the cpt-city website, see:
%          <a href="http://soliton.vm.bytemark.co.uk/pub/cpt-city/">http://soliton.vm.bytemark.co.uk/pub/cpt-city/</a>
% nSteps = number of colorsteps (optional)
%
% Note:
%  make sure to have downloaded the cpt-city package from:
%  <a href="http://soliton.vm.bytemark.co.uk/pub/cpt-city/pkg/cpt-city-cpt-1.42.zip">http://soliton.vm.bytemark.co.uk/pub/cpt-city/pkg/cpt-city-cpt-1.42.zip</a>
%  Unpack and add folder to the matlab search path
%
% Example:
%
% cmap = colormap_cpt('temperature');
% subplot(3,1,[1 2])
%   colormap(cmap)
%   [x,y,z] = cylinder(100:-1:10);surf(x,y,z);
%   camlight(300,20); view([-60 32]); shading flat;
%   material shiny; lighting gouraud; colorbar
% subplot(3,1,3)
%   plot(cmap); axis([1 size(cmap,1) -.01 1.01])
%
% See also: colormaps
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)