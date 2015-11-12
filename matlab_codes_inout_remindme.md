## remindme.m ##
Reminder using crontab and growl

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/remindme.m)

```
% remindme Reminder using crontab and growl
%
% [] = remindme(TIME,[TXT])
% 
% This function use growlnotify to send you a reminder with message TXT at
% time given by TIME (as returned by datenum).
%
% Inputs:
%	TIME is a serial date number as return by datenum.
%		It can also be a string of the form 'HH:MM' to use the current day.
%	TXT is a string
%
% Eg:
%	remindme(now+10/60/24,'Coffee break !');
%	remindme('16:00','Thea break !');
%
% Extra:
% 	If TIME is set to NaN, the function simply clean the crontab file of all Matlab reminders
%	
%
% Created: 2009-10-15.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)