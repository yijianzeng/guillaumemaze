## get\_plotlistdef.m ##
Display/return description of diagnostic files

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/get_plotlistdef.m)

```
%get_plotlistdef Display/return description of diagnostic files
%
% [LIST] = get_plotlistdef(MASTER,SUBDIR)
% 
% This function display a description of pre-defined plots/diag
% available with the MASTER.m in the folder SUBDIR
%
% Example:
% get_plotlistdef('hydro_selected_O2','.');
% % will list all hydro_selected_O2_pl* matlab files
%
% Rev. by Guillaume Maze on 2011-07-08: Get rid of variables sla, using fullfile
% Rev. by Guillaume Maze on 2011-03-28: Fix bug in determining the index of module
% Rev. by Guillaume Maze on 2009-05-29: Remove from the output diag without descriptions
% Created: 2006-07-12.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)