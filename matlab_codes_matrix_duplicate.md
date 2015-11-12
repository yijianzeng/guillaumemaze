## duplicate.m ##
Find duplicate values among a 1D table

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/duplicate.m)

```
% duplicate Find duplicate values among a 1D table
%
% [Vdup Idup] = duplicate(C,[PREC])
%
% Find duplicate values among a 1D table, ie identify values among
% C which are similar (to the approximate precisions PREC), give them back
% in Vdup and their occurences in C in Idup.
%
% Eg:
%	C = [1 3 2 2 3 7];
%	[Vdup Idup] = duplicate(C)
%
%	C = [1.9572    3.4854    2.8003    2.1419    3.4218    7.9157];
%	[Vdup Idup] = duplicate(C,0)
%	[Vdup Idup] = duplicate(C,1)
%	[Vdup Idup] = duplicate(C,2)
%
% Created: 2010-02-11.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)