## colormap.m ##
Color look-up table.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/colormap.m)

```
%COLORMAP Color look-up table.
%   COLORMAP(MAP) sets the current figure's colormap to MAP.
%   COLORMAP('default') sets the current figure's colormap to
%   the root's default, whose setting is JET.
%   MAP = COLORMAP retrieves the current colormap. The values
%   are in the range from 0 to 1.
%   COLORMAP(AX,...) uses the figure corresponding to axes AX
%   instead of the current figure.
%
%   A color map matrix may have any number of rows, but it must have
%   exactly 3 columns.  Each row is interpreted as a color, with the
%   first element specifying the intensity of red light, the second
%   green, and the third blue.  Color intensity can be specified on the
%   interval 0.0 to 1.0.
%   For example, [0 0 0] is black, [1 1 1] is white,
%   [1 0 0] is pure red, [.5 .5 .5] is gray, and
%   [127/255 1 212/255] is aquamarine.
%
%   Graphics objects that use pseudocolor  -- SURFACE and PATCH objects,
%   which are created by the functions MESH, SURF, and PCOLOR -- map
%   a color matrix, C, whose values are in the range [Cmin, Cmax],
%   to an array of indices, k, in the range [1, m].
%   The values of Cmin and Cmax are either min(min(C)) and max(max(C)),
%   or are specified by CAXIS.  The mapping is linear, with Cmin
%   mapping to index 1 and Cmax mapping to index m.  The indices are
%   then used with the colormap to determine the color associated
%   with each matrix element.  See CAXIS for details.
%
%   Type HELP GRAPH3D to see a number of useful colormaps.
%
%   COLORMAP is an M-file that sets the Colormap property of a figure.
%
%   See also HSV, CAXIS, SPINMAP, BRIGHTEN, RGBPLOT, FIGURE, COLORMAPEDITOR.
%
% Rev. by Guillaume Maze on 2010-11-04: Update colorbars if necessary
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)