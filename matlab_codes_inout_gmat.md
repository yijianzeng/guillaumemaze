## gmat.m ##
Grep a string into comments of Matlab routines within a given folder or file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/gmat.m)

```
% gmat Grep a string into comments of Matlab routines within a given folder or file
%
% [] = gmat(STRING,[[FOLDER],[OPT]])
% 
% This function sparses all *.m files into the optional directory FOLDER
% (default is ".") and look for occurances of STRING (case insensitive)
% into the file comments.
%
% OPT is also an optional parameter with values:
% 	OPT = 1 (default): will look for all comments
% 	OPT = 2: will look only for comment lines
%	OPT = 3: will look anywhere in the file
%
% Example:
% gmat('matrix',which('intro'))
%
%
% Created: 2009-06-23.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)