## smoother2Ddiff.m ##
Apply a diffusive smoother on a 2D field

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/smoother2Ddiff.m)

```
% SMOOTHER2DDIFF Apply a diffusive smoother on a 2D field
%
% [field_out,tmp3x,tmp3y] = smoother2Ddiff(field_in,dist_in1,dist_in2);
%
% Apply a diffusive smoother based on Weaver and Courtier, 2001.
%
% field_in:		field to be smoothed (masked with NaN)
% dist_in1/2:	scale in first/second direction
% field_out:	smoothed field
%
% The domain is assumed cyclic in both directions.
% If it is not, you want to mask edge points with NaNs.
%
% Created by Guillaume Maze on 2008-10-14.
% Developed with Gael Forget
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)