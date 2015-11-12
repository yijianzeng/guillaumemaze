## diag\_screen.m ##
Same as DISP but allow to print in a log file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/diag_screen.m)

```
% DIAG_SCREEN Same as DISP but allow to print in a log file
%
% [] = DIAG_SCREEN(MESSAGE,PID,[FIDLOGFILE],[FORMAT])
%
% Print to the screen and/or in a log file
% PID = 1 : Print to screen
% PID = 2 : Print to file LOGFILE (fid pointer)
%
% May also use: PID = [1 2]
% To make to implementation easier in big routines, a default set
% is available in global variables:
% DEFAULT IS:
% global 
% PID = [1 2]; % Screen and log file
% [LOGFILE] = fid_logfile; % 
% [FORMAT] = '%s\n';
%
% EG OF USE:
% global diag_screen_default
% diag_screen_default.PIDlist = [1 2];
% fid = fopen('myrun.log','w');
% diag_screen_default.fid = fid;
% diag_screen_default.forma = '%s\n';
% diag_screen('Hello world');
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)