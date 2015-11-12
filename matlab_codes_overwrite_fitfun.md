## fitfun.m ##
Used by FITDEMO.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/overwrite/fitfun.m)

```
%FITFUN Used by FITDEMO.
%   FITFUN(lambda,t,y,handle) returns the error between the data and the values
%   computed by the current function of lambda.
%
%   FITFUN assumes a function of the form
%
%     y =  c(1)*exp(-lambda(1)*t) + ... + c(n)*exp(-lambda(n)*t)
%
%   with n linear parameters and n nonlinear parameters.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)