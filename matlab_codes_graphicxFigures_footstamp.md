## footstamp.m ##
Create the default footnote for figure

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxFigures/footstamp.m)

```
% footstamp Create the default footnote for figure
%
% STR = footstamp([TYP])
% 
% Create the default footnote string for figure
%
% TYP (optional):
%	1 (default) : 
%		>> footstamp
%		macbook://Users/gmaze/work/Postdoc/work/main/hydrolpo
%	2: 
%		>> footstamp(2,[mfilename('fullpath') '.m'])
%		(macbook) file://Users/gmaze/work/Postdoc/work/main/hydrolpo/hydro_selected_viewdates.m
%	3: Same as 2 but output is a cell of string
%	
%
% Rev. by Guillaume Maze on 2012-02-13: Added option 3 for cell outputs
% Created: 2009-07-22.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)