## packver.m ##
Manage Package Version file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/packver.m)

```
% packver Manage Package Version file
%
% pack_info = packver(PACK_DIR,ACTION,{'PROP','VAL'},{'PROP','VAL'},...)
% 
% Manage a Package Version file version.ver
%
% Inputs:
%	PACK_DIR: path to package
%	ACTION: 
%		'r': read package version information
%		'w': create version.ver version file
%		'u': update any property of the version file
%	PROP: One of the following properties:
%		'Name' with VAL (string): Package description
%		'Version' with VAL (string): Package version
%		'Release' with VAL (string): Older Matlab release compatible with the package
%		'Date' with VAL (datenum): Last update of the package
%
% Outputs:
%	pack_info: a structure with package informations.
%
% Created: 2010-04-15.
% Rev. by Guillaume Maze on 2011-03-04: Changed default package characteristics
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)