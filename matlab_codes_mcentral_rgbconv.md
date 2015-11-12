## rgbconv.m ##
Convert hex color to or from matlab rgb vector.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/rgbconv.m)

```
%RGBCONV   Convert hex color to or from matlab rgb vector.
%   RGB = RGBCONV(HEX)  where HEX is a string of hexadecimal numbers
%      'RRGGBB' where the parts RR, GG, BB are two digit hexadecimal
%      numberes corresponding to the strengths of the colors red,
%      green and blue. RGB is the matlab rgb-vector.
%   RGB = RGBCONV(HEX)  where HEX is a string matrix of the form
%      ['RR';'GG';'BB'], or a cell string {'RR','GG','BB'}, or
%   RGB = RGBCONV('RR','GG','BB')
%   [R,G,B] = RGBCONV(...)  gives the corresponding matlab rgb-values
%   as scalar values in R, G and B correspondingly.
%
%   HEX = RGBCONV(RGB)  where RGB is a matlab rgb-vector with
%      three elements each corresponding to strengs of
%      red, green and blue and ranging between 0 and 1.
%   HEX = RGBCONV(R,G,B)  where R, G and B are scalar values
%      ranging between 0 and 1 each corresponding to red, green
%      and blue.
%      HEX is a string containing the hex values and is of length 6.
%   ['RR','GG','BB'] = RGBCONV(...)  gives the corresponding hex
%      values as two character strings 'RR', 'GG' and 'BB'
%
%   Examples:
%      rgbconv([.1 .2 .3])
%      rgbconv(.55,.6,.12)
%      [r,g,b]=rgbconv([.1 .2 .3])
%      rgbconv('1a334d')
%      rgbconv('1a','33','4d')
%      [r,g,b]=rgbconv({'F1','2A','55'})
%
%   See also COLORMAP.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)