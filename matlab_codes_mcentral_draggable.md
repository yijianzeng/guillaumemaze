## draggable.m ##
- Make it so that a graphics object can be dragged in a figure.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/draggable.m)

```
% DRAGGABLE - Make it so that a graphics object can be dragged in a figure.
%   This function makes an object interactive by allowing it to be dragged
%   accross a set of axes, following or not certain constraints. This
%   allows for intuitive control elements which are not buttons or other
%   standard GUI objects, and which reside inside an axis. Typical use
%   involve markers on an axis, whose position alters the output of a
%   computation or display
% 
%   >> draggable(h);
%   
%   makes the object with handle "h" draggable. Use the "Position" property
%   of the object to retrieve its position, by issuing a get(h,'Position')
%   command.
%
%   >> draggable(h,...,motionfcn)
%
%   where "motionfcn" is a function handle, executes the given function
%   while the object is dragged. Handle h is passed to motionfcn as an
%   argument. Argument "motionfcn" can be put anywhere after handle "h".
%
%   >> draggable(h,...,constraint,p);
%
%   enables the object with handle "h" to be dragged, with a constraint.
%   Arguments "constraint" (a string) and "p" (a vector) can be put
%   anywhere after handle "h".
%
%   The argument "constraint" may be one of the following strings:
%
%       'n' or 'none':          The object is unconstrained (default).
%       'h' or 'horizontal':    The object can only be moved horizontally.
%       'v' or 'vertical':      The object can only be moved vertically.
%
%   The argument "p" is an optional parameter which depends upon the
%   constraint type:
%
%   Constraint      p                   Description
%   -----------------------------------------------------------------------
%
%   'none'          [x1 x2 y1 y2]       Drag range (for the object's outer
%                                       limits, from x1 to x2 on the x-axis
%                                       and from y1 to y2 on the y-axis).
%                                       Default is the current axes range.
%                                       Use "inf" if no limit is desired.
%
%   'horizontal'    [xmin xmax]         Drag range (for the object's outer
%                                       limits). Default is the x-axis
%                                       range. Use "inf" if no limit is
%                                       desired.
%
%   'vertical'      [ymin ymax]         Drag range (for the object's outer
%                                       limits). Default is the y-axis
%                                       range. Use "inf" if no limit is
%                                       desired.
%
%   -----------------------------------------------------------------------
%
%   >> draggable(h,'off')
%
%   returns object h to its original, non-draggable state.
%
%   See the source code (e.g. by issuing "type draggable" at the Matlab 
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)