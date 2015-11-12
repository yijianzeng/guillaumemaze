## dragdemo.m ##
Demo for the draggable.m

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/dragdemo.m)

```
% DRAGDEMO Demo for the draggable.m
%   This function is a demo for the draggable.m function and should be
%   distributed along with it. It basically presents some of draggable.m's
%   features: users of draggable.m are invited to read dragdemo's source.
%
%   >> dragdemo(demotitle);
%
%   runs the demo which title is contained in the string demotitle.
%   Available demos are:
%
%   'crosshair'     A draggable crosshair is drawn; its movements are
%                   limited so that its center never leaves the axes. This
%                   is the default demo.
%
%   'dragtest'      Some graphical objects (such as rectangles, lines,
%                   patches and plots) are drawn, following various
%                   constraints. For more details, please read the comments
%                   in the source code.
%
%   'snapgrid'      An example on how to use draggable's "motionfcn"
%                   argument so that a draggable object snaps to a grid.
%
%   'polymove'      A polygon with draggable vertices is drawn;
%                   draggable's "motionfcn" argument is used to redraw the
%                   polygon each time a vertex is moved.
%
% Franois Bouffard
% fbouffar@gel.ulaval.ca
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)