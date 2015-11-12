## xticklabel\_rotate.m ##
hText = xticklabel\_rotate(XTick,rot,XTickLabel,varargin) Rotate XTickLabel

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/xticklabel_rotate.m)

```
%hText = xticklabel_rotate(XTick,rot,XTickLabel,varargin)     Rotate XTickLabel
%
% Syntax: xticklabel_rotate
%
% Input:    
% {opt}     XTick       - vector array of XTick positions & values (numeric) 
%                           uses current XTick values or XTickLabel cell array by
%                           default (if empty) 
% {opt}     rot         - angle of rotation in degrees, 90 by default
% {opt}     XTickLabel  - cell array of label strings
% {opt}     [var]       - "Property-value" pairs passed to text generator
%                           ex: 'interpreter','none'
%                               'Color','m','Fontweight','bold'
%
% Output:   hText       - handle vector to text labels
%
% Example 1:  Rotate existing XTickLabels at their current position by 90
%    xticklabel_rotate
%
% Example 2:  Rotate existing XTickLabels at their current position by 45 and change
% font size
%    xticklabel_rotate([],45,[],'Fontsize',14)
%
% Example 3:  Set the positions of the XTicks and rotate them 90
%    figure;  plot([1960:2004],randn(45,1)); xlim([1960 2004]);
%    xticklabel_rotate([1960:2:2004]);
%
% Example 4:  Use text labels at XTick positions rotated 45 without tex interpreter
%    xticklabel_rotate(XTick,45,NameFields,'interpreter','none');
%
% Example 5:  Use text labels rotated 90 at current positions
%    xticklabel_rotate([],90,NameFields);
%
% Note : you can not RE-RUN xticklabel_rotate on the same graph. 
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)