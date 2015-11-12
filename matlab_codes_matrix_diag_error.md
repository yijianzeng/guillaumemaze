## diag\_error.m ##
Propagate error estimates for misc operators

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/diag_error.m)

```
% diag_error Propagate error estimates for misc operators
%
% er = diag_error(typeOP,A,Aer,varargin)
% 
% Combine error estimates for misc operators/
% 
% Eg:
% 
% To compute the error of the sum of elements (A) given 
% their errors (Aer):
% er = diag_error('+',A,Aer);
% 
% To compute the error of the product of A elements with B elements (A) 
% given their errors (Aer and Ber):
% er = diag_error('*',A,Aer,B,Ber);
%
% Created: 2010-11-12.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)