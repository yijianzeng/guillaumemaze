## mtags.m ##
Read/write tags to Matlab function header section

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/mtags.m)

```
% mtags Read/write tags to Matlab function header section
%
% tags_list = mtags(FILE)
% 	Read the list of tags documented in a Matlab script FILE
% 
% tags_list = mtags(FILE,'add',TAGS)
% 	Add TAGS to the list of tags documented in Matlab script FILE
%
% tags_list = mtags(FILE,'remove',TAGS)
% 	Remove TAGS from the list of tags documented in Matlab script FILE
%
% bool = mtags(FILE,'has',TAGS)
% bool = mtags(FILE,'hasany',TAGS)
% 	Return true if one of TAGS is listed in tags documented in Matlab script FILE
%
% bool = mtags(FILE,'hasall',TAGS)
% 	Return true if all TAGS are listed in tags documented in Matlab script FILE
%
% Note that all methods pointing to a function are supported:
% 	mtags(@stophere)
% 	mtags('stophere')
% 	mtags(which('stophere'))
% 
% Created: 2013-12-09.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)