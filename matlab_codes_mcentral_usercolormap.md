## usercolormap.m ##
Create a color map.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/usercolormap.m)

```
% USERCOLORMAP Create a color map.
%
%    USERCOLORMAP(COLOR1,COLOR2,COLOR3,...) creates a colormap
%    with colors specified by 1x3 vectors (COLOR1, COLOR2,
%    COLOR3...).
%
%    When the number of input colors are three for example,
%    the function linearly interpolates every column of a
%    3x3 matrix [COLOR1;COLOR2;COLOR3] to 256 values, which
%    is to be used as an input to COLORMAP. It means that
%    colors between those you specified change gradually.
%
%    (Example 1)
%    color1 = [1 0 0];
%    color2 = [1 1 1];
%    color3 = [0 0 1];
%    figure;
%    colormap(usercolormap(color1,color2,color3)),colorbar;
%
%
%    If you put a number (>0) as the last input argument
%    (USERCOLORMAP(...,NUM)), then the intensity scaling is
%    respected by automatically adjusting colors, in such a
%    way that the first color be the darkest (or lightest)
%    and the last be the lightest (or darkest). This is useful
%    when figures have to be printed out or photocopied in
%    grayscale.
%
%    When using this option, n-th intensity I(n) is expressed by
%    I(n) = I(1) + (I(256)-I(1))*((n-1)/255)^NUM.
%    When NUM = 1, then the scaling is linear (as in 
%    colormap(gray)). 1.2 can be a good compromise between
%    color map and intensity scale. You can check how it
%    looks in intensity (black and white) by exporting a
%    figure to a black/white eps format.
%
%    (Example 2)
%    color1 = [0 0 0];
%    color2 = [1 0 0];
%    color3 = [0.2 0.2 1];
%    color4 = [1 1 0];
%    color5 = [1 1 1];
%    figure;
%    C = usercolormap(color1,color2,color3,color4,color5,1);
%    colormap(C),colorbar;
%
%    You can also create an m-script like
%    %%%%%%
%    function C = mycolor
%    C = usercolormap([0 0 0],[1 0 0],[1 1 1]);
%    %%%%%%
%    and call this colormap by 'colormap(mycolor)'.
%
%    See also COLORMAP.
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)