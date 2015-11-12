## figs2pdf.m ##
Save several figures in 1 pdf file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxFigures/figs2pdf.m)

```
% figs2pdf Save several figures in 1 pdf file
%
% [] = figs2pdf(PDFFILE,[FIGLIST])
% 
% Save several figures in 1 pdf file with multiple pages.
%
% Inputs:
%	PDFFILE: the output pdf file name (without the pdf extension)
%	FIGLIST(optional): the list of figure's handle to include in the file
%		If not specified (default) save all open figures.
%
% Rq:
%	- To insert a blank page you can use an empty figure and insert it where you want.
%	- To insert text, create a invisible axes with your text.
%	- Eg:
%		t = 0:pi/50:10*pi;
%		f(1)=builtin('figure');set(gca,'visible','off');
%			text(.5,.5,sprintf('A list of figures from Matlab\nPDF TEST !'),'fontweight','bold','horizontalalignment','center','fontsize',16);
%		f(2)=figure;plot(t,cos(t));
%		f(3)=builtin('figure')
%		f(4)=figure;plot3(sin(t),cos(t),t);
%		figs2pdf('toto',f)
%
%	- This routine uses the ps2pdf.m script from Richard Quist:
%	http://www.mathworks.com/matlabcentral/fileexchange/19516-ps2pdf
%
% Created: 2010-04-02.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)