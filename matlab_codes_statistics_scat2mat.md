## scat2mat.m ##
Map scattered data onto a regular grid

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/scat2mat.m)

```
% scat2mat Map scattered data onto a regular grid
%
% M = scat2mat(Xi,Yi,Zi,Xb,Yb) Map values Zi scattered along two irregular Xi,Yi 
% 	axis coordinates onto a regular grid defined by meshed grid axis Xb,Yb. See bin2mat 
% 	for more details.
%
% M = scat2mat(Xi,Yi,Zi,Xb,Yb,@fun) Map values Zi scattered along irregular Xi,Yi 
% 	coordinates onto a regular grid defined by meshed axis Xb,Yb. The function @fun 
% 	is used to agregate values. See bin2mat for more details.
% 
% [M IND] = scat2mat(Xi,Yi,Zi,Xb,Yb,@fun,@ope,val) Map values Zi scattered along 
% 	irregular Xi,Yi coordinates onto a regular grid defined by meshed axis Xb,Yb. 
% 	The function @fun is used to agregate values. IND is the list of indexes in Zi
% 	for which the operator @ope is satisfied with value val on the normalized map
% 	values.
% 
% Created: 2013-11-07.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)