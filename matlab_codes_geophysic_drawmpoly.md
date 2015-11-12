## drawmpoly.m ##
drawpoly Draw a polygon on a map (using m\_map)

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/drawmpoly.m)

```
% drawpoly Draw a polygon on a map (using m_map)
%
% [LON LAT HL] = drawmpoly;
% 
% Draw a polygon on a map by mouse clicks and return coordinates
% of the closed polygon.
%
% Outputs:
%	LON: Longitude of the polygon points
%	LAT: Latitude of the polygon points
%	HL: Handle of the polygon plotted on the map
%
% Use
% 	delete(findobj(gcf,'tag','drawmpoly'));
% to remove all polygons from the map.
% 
% Created: 2010-05-05.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)