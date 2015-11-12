## dashline.m ##
Function to produce accurate dotted and dashed lines

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/overwrite/dashline.m)

```
%DASHLINE  Function to produce accurate dotted and dashed lines
%   DASHLINE(XDATA, YDATA, DASH1, GAP1, DASH2, GAP2, ...) plots 
%   the data XDATA and YDATA usig a two dash linestyle. The 
%   function allows the lengths of the dashes to be specified. 
%   DASH1 is the length of the first dash; GAP1 is the length of 
%   the first gap; DASH2 is the length of the second  dash and 
%   GAP2 is the length of the second gap, with all lengths being 
%   in millimeters. The two dash pattern is repeated along the 
%   length of the line. The routine is designed to allow greater
%   control over the linestyle than is available using PLOT.
%
%   Additional inputs may be given to specify line properties. 
%   These are passed through to the plot function. 
%
%   DASH1 or DASH2 may be strings specifying plot symbols. A 
%   dashlength of 0 will cause a dot to be plotted. If GAP1 and 
%   GAP2 are 0 then the arguments are simply passed through to a 
%   plot command
%
%   For example: 
%   clf;
%   dashline([1:10],rand(1,10),1,1,1,1) 
%      %produces a dashed line with 1mm dashes and 1mm gaps
%   hold on;
%   dashline([1:10],rand(1,10),4,2,'o',2,'markerfacecolor','y',...
%      'color','k') 
%      %produces a line with black dashes and yellow centred circles
%
%   [H1, H2]=DASHLINE(...) Outputs are handles to the plotted 
%      lines and markers
%
%   DASHLINE works by calculating the distance along the line to be 
%   plotted, using the existing axes position. If HOLD is OFF when 
%   DASHLINE is called, then the axis limits are set automatically; 
%   otherwise the existing limits are used. DASHLINE then 
%   interpolates XDATA and YDATA at the positions of the start and 
%   end of the dashes, using NaN's to lift the pen. Rescaling the 
%   axes after DASHLINE has been called, or changing the limits, or 
%   changing from log to linear plots, will mean that the dashes no 
%   longer have the specified lengths. This routine does not calculate 
%   distances correctly if the axes DataAspectRatio or 
%   PlotBoxAspectRatio have been manually specified. The lines will 
%   not display properly in a call to LEGEND.
%
%   Kluged together by Edward Abraham (e.abraham@niwa.cri.nz) 
%   27-Sept-2002 Minor change made so that it works with Matlab 6.5
%   27-June-2002 Original version
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)