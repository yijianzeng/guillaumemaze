## fopenn.m ##
Open a file whithout taking care of slash in file name

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/fopenn.m)

```
% FOPENN Open a file whithout taking care of slash in file name
%
% This the same function as the built-in but before calling it,
% a test on the filename format is done: / on unix system are replaced
% by \ of windows if the 'computer' Matlab command return PCWIN.
%
%    See also FOPEN, FCLOSE, FREWIND, FREAD, FWRITE, FPRINTF.
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)