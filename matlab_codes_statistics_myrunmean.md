## myrunmean.m ##
Perform running mean on an array

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/myrunmean.m)

```
% MYRUNMEAN Perform running mean on an array
%
% A = myrunmean(a,NF,bool,dirm)
% compute runing mean of a in direction dirm with
% NF mean, i.e at each time step
%  A(i) --> mean( a(i-NF/2:i+NF/2) ,dirm )
%
% if bool == 1, A has only the N-NF elemts
% if bool == 0, A is Nan outside and has N elmts
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)