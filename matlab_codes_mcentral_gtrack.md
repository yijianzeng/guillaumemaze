## gtrack.m ##
Track mouse position and show coordinates in figure title.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/gtrack.m)

```
% GTRACK Track mouse position and show coordinates in figure title.
% 
% 	GTRACK Activates GTRACK. Once it is active the mouse position is
% 	constantly tracked and printed on the figure title. A left-click will
% 	print the coordinates in the command line and store them. Clicking the
% 	mouse right button deactivates GTRACK.
% 
% USAGE
% 	gtrack() tracks the mouse and prints coordinates in the command line.
% 
% 	clickData = gtrack() will return the click positions in clickData using
% 	UIWAIT. Matlab will be in wait mode until the user finishes clicking.
% 
% 	gtrack('newVar') tracks the mouse and creates a new variable in the
% 	base workspace called 'newVar' with the click coordinates. This mode
% 	does not use UIWAIT.
%
%	gtrack([],titleFormat) uses titleFormat as the format string for
%	printing the mouse coordinates in the title.
%
%
% 2007 Jose F. Pina, Portugal
% http://www.mathworks.com/matlabcentral/fileexchange/loadFile.do?objectId=15099
% 
% REVISION 
%	23-05-2007	- created
%	30-05-2007	- fixed case matches, nested functions instead of globals,
%				  improved output modes
%	31-05-2007	- added option to choose coordinates format
%
% CREDITS
%	initial version - based on GTRACE
%	http://www.mathworks.com/matlabcentral/fileexchange/loadFile.do?objectId=3832&objectType=file
% 	Furi Andi Karnapi and Lee Kong Aik, DSP Lab, School of EEE, Nanyang Technological University
% 	Singapore, March 2002
%
%	improved version - thanks for the hints to John D'Errico
%   http://www.mathworks.com/matlabcentral/fileexchange/loadAuthor.do?objectType=author&objectId=801347
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)