## datevec2doy.m ##
Takes a date vector and returns the day of year, known incorrectly in the

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/datevec2doy.m)

```
% Takes a date vector and returns the day of year, known incorrectly in the
% Geophysical community as the julian calender day, i.e. 12/31/2005
% is returned as day 365, day 06/22/2010 is returned as 173, etc... The
% function is vectorized. This function needs etime.m (R2009a and later).
% 
% USAGES
% julday = datevec2doy(mydate)
% 
% INPUT
% mydate:   Either a 6xN or Nx6 array of date vectors, as output by
%           functions like datevec.
% 
% OUTPUT
% julday:   An Nx1 array of julian days.
% 
% -----------------------------------------------------------------------
% EXAMPLE
% %Take the current day and add normally distributed random days to the
% %date.
% 
% tadd          = randn(1,12);
% mydate        = datevec(now)';
% mydate        = repmat(mydate,1,12);
% mydate(2,:)   = mydate(2,:) + tadd;
% day           = datevec2doy(mydate);
% -----------------------------------------------------------------------
% Latest Edit: 24.June.2010
% Joshua D Carmichael
% josh.carmichael@gmail.com
%-----------------------------------------------------------------------
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)