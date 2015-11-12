## linerr.m ##
Plot a line whose thickness represents error bars (using patch)

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/linerr.m)

```
% LINERR Plot a line whose thickness represents error bars (using patch)
%
% P = LINERR(TIM,VAL,ERR,[C]) plot the timeserie VAL(TIM)+/-ERR(TIM) 
% as a patch centered on VAL(TIM)and whose thickness is the error bar 
% ERR(TIM). C is the color of the patch. By default it is set to gray.
% 
% [P PL] = LINERR(TIM,VAL,ERR,C,'core',[ARGS]) same as the default call but also 
% superimpose VAL(TIM) as a plot(VAL,TIM,[ARGS]) on the patch.
%
% Outputs:
% 	P: patch handle.
% 	PL: plot handle.
%
% Created: 2013-07-18.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)