## convX.m ##
Convert longitude convention

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/convX.m)

```
% convX Convert longitude convention
%
% lon = convX(lon,[idconv])
% 
% Convert longitude from one convention to another:
% Inputs:
% 	lon: The longitudes to convert (any dimensions)
% 	idconv:	One of the following:
% 		1 (default): Convert to longitude East, ie: 0 < lon < 360
% 		0: Convert to longitude East/West, ie: -180 < lon < 180
% 		2: Convert to longitude East with sorted axis, ie: 0 < lon < 360
% 
% Created: 2013-02-21.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)