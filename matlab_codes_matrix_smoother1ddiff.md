## smoother1Ddiff.m ##
Apply a diffusive smoother on a 1D field

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/smoother1Ddiff.m)

```
% smoother1Ddiff Apply a diffusive smoother on a 1D field
%
% field_out = smoother1Ddiff(field_in,dist_in1);
%
% Apply a diffusive smoother based on Weaver and Courtier, 2001.
%
% field_in:	field to be smoothed (masked with NaN)
% dist_in1:	scale in first direction
% field_out:	smoothed field
%
% The domain is assumed cyclic.
% If it is not, you want to mask edge points with NaNs.
%
% Created by Guillaume Maze on 2009-11-24.
% Developed with Gael Forget
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)