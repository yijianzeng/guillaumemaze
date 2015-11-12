## wsload.m ##
Load all (or list of) variables of the base workspace into a function workspace

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/wsload.m)

```
% wsload Load all (or list of) variables of the base workspace into a function workspace
%
% wsload() Load all variables from the base workspace to the caller workspace.
% 
% wsload('var') Load variable named 'var' from the base workspace to the caller workspace.
% 
% wsload('pat*') List all variables with names 'pat*' and load from the base workspace to the caller workspace.
% 
% wsload({'var1','var2'}) Load variables named 'var1' and 'var2' from the base workspace to the caller workspace.
% 
% Created: 2009-11-05.
% Rev. by Guillaume Maze on 2013-07-25: Added wild card * loading type and modified help
% Rev. by G. Maze on 2011-07-28: Change warning to error when trying to load a nonexistent variable.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)