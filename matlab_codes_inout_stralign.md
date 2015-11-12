## stralign.m ##
Align/Justify a string within a given sized blank space

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/stralign.m)

```
% stralign Align/Justify a string within a given sized blank space
%
% STR = stralign(L,STR,JUST)
% 
% Justify to JUST string STR within a blanck space of length L.
%	L is double, STR is char and JUST can be any string of:
%		'right','left','center'.
%
% Example:
%	t = stralign(30,'hello world !','right')
% will produce:
%	t =  '                 hello world !'
%	length(t) = 30
%
% See also: strjust
%
% Created: 2011-03-07.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)