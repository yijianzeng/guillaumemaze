## growl.m ##
Send a notification to Growl

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/growl.m)

```
% growl Send a notification to Growl
%
% [] = growl(MESSAGE,[TITLE,STICKY,PRIORITY])
% 
% Send a notification to Growl.
%
% Inputs:
%	MESSAGE (double or string): 1 single line message
%	TITLE (double or string): Title of the notification
%	STICKY: 0 (default) or 1 to indicate if the notification should stick on screen
%	PRIORITY (double): Priority of the notification (0 by default)
%		Priority is not supported by all displays, so this may be ignored.
%
% If no title is specified, the routine caller is indicated.
%
% Example:
%	growl('routine starts');
%	% Your routine here
%	growl('routine ends');
%
% Created: 2009-09-25.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)