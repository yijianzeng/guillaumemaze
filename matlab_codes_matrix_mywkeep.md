## mywkeep.m ##
Keep part of a vector or a matrix.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/mywkeep.m)

```
% MYWKEEP Keep part of a vector or a matrix.
%   For a vector:
%   Y = WKEEP(X,L,OPT) extracts the vector Y 
%   from the vector X. The length of Y is L.
%   If OPT = 'c' ('l' , 'r', respectively), Y is the central
%   (left, right, respectively) part of X.
%   Y = WKEEP(X,L,FIRST) returns the vector X(FIRST:FIRST+L-1).
%
%   Y = WKEEP(X,L) is equivalent to Y = WKEEP(X,L,'c').
%
%   For a matrix:
%   Y = WKEEP(X,S) extracts the central part of the matrix X. 
%   S is the size of Y.
%   Y = WKEEP(X,S,[FIRSTR,FIRSTC]) extracts the submatrix of 
%   matrix X, of size S and starting from X(FIRSTR,FIRSTC).
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)