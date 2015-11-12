## vivid.m ##
Creates a Personalized Vivid Colormap

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/vivid.m)

```
% VIVID Creates a Personalized Vivid Colormap
%  VIVID(...) Creates a vivid colormap with custom settings
%
%   Inputs:
%       M - (optional) an integer between 1 and 256 specifying the number
%           of colors in the colormap. Default is 128.
%       MINMAX - (optional) is a 1x2 vector with values between 0 and 1
%           representing the intensity range for the colors, which correspond
%           to black and white, respectively. Default is [0.15 0.85].
%       CLRS - (optional) either a Nx3 matrix of values between 0 and 1
%           representing the desired colors in the colormap
%               -or-
%           a string of characters that includes any combination of the
%           following letters:
%               'r' = red, 'g' = green, 'b' = blue
%               'y' = yellow, 'c' = cyan, 'm' = magenta
%               'o' = orange, 'l' = lime green, 'a' = aquamarine
%               's' = sky blue, 'v' = violet, 'p' = pink
%               'k' or 'w' = black/white/grayscale
%
%   Outputs:
%       CMAP - an Mx3 colormap matrix
%
%   Example:
%       % Default Colormap
%       imagesc(sort(rand(200),'descend'));
%       colormap(vivid); colorbar
%
%   Example:
%       % Mapping With 256 Colors
%       imagesc(peaks(500))
%       colormap(vivid(256)); colorbar
%
%   Example:
%       % Mapping With Full Intensity Range
%       imagesc(peaks(500))
%       colormap(vivid([0 1])); colorbar
%
%   Example:
%       % Mapping With Light Colors
%       imagesc(peaks(500))
%       colormap(vivid([.5 1])); colorbar
%
%   Example:
%       % Mapping With Dark Colors
%       imagesc(peaks(500))
%       colormap(vivid([0 .5])); colorbar
%
%   Example:
%       % Mapping With Custom Color Matrix
%       imagesc(peaks(500))
%       clrs = [1 0 .5; 1 .5 0; .5 1 0; 0 1 .5; 0 .5 1; .5 0 1];
%       colormap(vivid(clrs)); colorbar
%
%   Example:
%       % Mapping With Color String
%       imagesc(peaks(500))
%       colormap(vivid('roylgacsbvmp')); colorbar
%
%   Example:
%       % Colormap With Multiple Custom Settings
%       imagesc(sort(rand(300,100),'descend'));
%       colormap(vivid(64,[.1 .9],'rwb')); colorbar
%
% See also: jet, hsv, gray, hot, copper, bone
%
% Author: Joseph Kirk
% Email: jdkirk630@gmail.com
% Release: 1.0
% Date: 07/25/08
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)