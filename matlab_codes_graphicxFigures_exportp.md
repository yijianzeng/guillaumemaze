## exportp.m ##
Export a figure to A4 color PDF format

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxFigures/exportp.m)

```
% exportp Export a figure to A4 color PDF format
%
% exportp(GCF,[ORIENTATION,FILE,KEEPFOOTNOTE])
%
%   Export a figure GCF to A4 color pdf format
%   Default output file is: 'fig.pdf' in current directory.
%
%   ORIENTATION: Set the orientation of the figure.
%       ORIENTATION=0 : Portrait (default)
%       ORIENTATION=1 : Landscape
%       ORIENTATION=2 : Crop PDF to plot (like eps print)
%
%	FILE: File name as a string. Default is 'fig'. Do not need to
%		specify the .pdf extension.
%
%	KEEPFOOTNOTE is an optionnal parameter:
%		KEEPFOOTNOTE=0 : Print pdf without the footnote.
%		KEEPFOOTNOTE=1 : Keep it (default)
%
% Note:
%	- you don't need to use figure's footnotes for this
%		function to work. To learn more see function 'footnote'.
%	- Informations about the file's name and orientation are stored
%		in the figure datas, so that you can use function 'reexportp'.
%	
% See also:
%	figure_land, figure_tall, footnote, fnote, reexportp, expt
%
% Created: 2009-04-22.
% Rev. by Guillaume Maze on 2011-03-04: Made it stand alone function
% Rev. by Guillaume Maze on 2010-10-21: Add cropped pdf option
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)