## ConsoleProgressBar.m ##
Console progress bar for long-running operations

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/ConsoleProgressBar.m)

```
%ConsoleProgressBar Console progress bar for long-running operations
%
% Description:
%   This class creates a console progress bar (status bar) 
%   for long-running operations.
%
%   It is possible to measure the elapsed and remained time of progress.
%
%
% Usage:
%   cpb = ConsoleProgressBar();
%
%
% Example:
%   % Create Instance
%   cpb = ConsoleProgressBar();
%
%   % Set progress bar parameters
%   cpb.setLeftMargin(1);   % progress bar left margin
%   cpb.setTopMargin(1);    % rows margin
%   
%   cpb.setLength(40);      % progress bar length: [.....]
%   cpb.setMinimum(0);      % minimum value of progress range [min max]
%   cpb.setMaximum(100);    % maximum value of progress range [min max]
%   
%   cpb.start();
%   
%   for k = 0:100
%       userText = sprintf('Progress: [%d/%d]', k, 100);
%       
%       cpb.setValue(k);       	% update progress value
%       cpb.setText(userText)   % update user text
%       
%       pause(0.025)
%   end
%   
%   cpb.stop();
%
%
% See also WAITBAR
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)