## figures2htm.m ##
Writes all open figures to .png files and integrates them in a html file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxFigures/figures2htm.m)

```
% figures2htm Writes all open figures to .png files and integrates them in a html file
% or
% figures2htm(reportdir,basename)
%
% 1) Writes all open figures to .png files and integrates them in a html file
% which opens the figure to full screen if clicked. If the figure has a
% name rather than a number, this will be part of the filename
% 2) and creates an index.htm for easy acces of several results
% Especially handy when a function has to be run often and produces quite
% some images.
% 3) writes relative links, so the entire dir can be copied and links still
% work
% 4) Works NOT in Firefox, sorry for that. The generated .htm code is quite
% crude, IE does render this.
%
% An index.htm is built for easy access of several reports, made for
% rerunning this code from different functions and datasources. The same
% reportdir should be used.
% and
% write variables to this htm-file with relevant images in same dir.
% 
% USAGE : 
%  'reportdir'  = Directory where to write, should end with a backslash
%  'basename'   = name of dataset which is being plotted
% 'functionname'= name of function that calls figure_report, if none given
%                 'unknown_' will be used.
% the 2 last mentioned names will be incorporated in the filenames and/or 
% sub-dir names, which is handy for browsing results
% base
% 
% EXAMPLE :
% figure
% set(gcf,'NumberTitle','off','Name','Sinewave');
% plot(sin(0:0.1:6.3));
% 
% figure
% plot(rand(40,1));
% 
% figure
% set(gcf,'Name','Peaks'); 
% surf(peaks);
% 
% figures2htm('C:\figdemo\','demo','function') 
% figures2htm('C:\figdemo\','demo')
%
%
% N.J.de Grooth
%  2006
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)