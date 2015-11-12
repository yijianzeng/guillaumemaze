## datenumserie.m ##
Create a time serie with datenum

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/datenumserie.m)

```
% datenumserie Create a time serie with datenum
%
% DTNUM = datenumserie(Y,MO,[D,M,S])
% 
% Create a timeseries of datenum: return the serial date
% numbers for corresponding elements of the Y, MO (year, month)
% and eventually D, M or S (day, minutes, seconds).
%
% This function is a fix for the fact that when calling:
%	datenum(2002:2003,1:12,1,0,0,0)
% the outcome is a 12 elements array similar to:
%	datenum(2002,1:12,1,0,0,0)
% which is not satisfactory.
% 
% When calling:
%	datenumserie(2002:2003,1:12,1,0,0,0)
% the outcome is the expected time serie of 24 elements 
% between 2002/01 and 2003/12.
%
% Created: 2011-06-17.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)