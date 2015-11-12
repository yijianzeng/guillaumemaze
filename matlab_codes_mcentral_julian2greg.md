## julian2greg.m ##
This function converts the Julian dates to Gregorian dates.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/julian2greg.m)

```
%julian2greg This function converts the Julian dates to Gregorian dates.
%
% 0. Syntax:
% [day,month,year,hour,min,sec,dayweek] = julian2greg(JD)
%
% 1. Inputs:
%     JD = Julian date.   
%
% 2. Outputs:
%     year, month, day, dayweek = date in Gregorian calendar.
%     hour, min, sec = time at universal time.
%
% 3. Example:
%  >> [a,b,c,d,e,f,g,h] = julian2greg(2453887.60481)
%  a = 
%     2006      
%  b =
%     6
%  c =
%     1
%  d =
%     2
%  e =
%     30
%  f =
%     56
%  g = 
%     Thursday
%  h =
%       1     6     2006     2     30     56
%
% 4. Notes:
%     - For all common era (CE) dates in the Gregorian calendar.
%     - The function was tested, using  the julian date converter of U.S. Naval Observatory and
%     the results were similar. You can check it.
%     - Trying to do the life... more easy with the conversions.
%
% 5. Referents:
%     Astronomical Applications Department. "Julian Date Converter". From U.S. Naval Observatory.
%               http://aa.usno.navy.mil/data/docs/JulianDate.html
%     Duffett-Smith, P. (1992).  Practical Astronomy with Your Calculator.
%               Cambridge University Press, England:  pp. 8,9.
%
% Gabriel Ruiz Mtz.
% Jun-2006
% ____________________________________________________________________________________________
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)