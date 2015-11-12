## sublist.m ##
Subplot indices for portrait/landscape 2 ranks loops plot

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/graphicxPlots/sublist.m)

```
% sublist Subplot indices for portrait/landscape 2 ranks loops plot
%
% plist = sublist(n1,n2,orient)
% 
% Inputs:
%	n1,n2: two integers
% 	orient can be:
%		'portrait' or 1
%		'landscape' or 0
% Outputs:
% 	plist is n1*n2 table of subplot indices
%
% Note that Portrait/landscape reference is for nv > ns
%
% Exampe:
% ns=3; nv=4;
% plist1 = sublist(ns,nv,'landscape');iw1=ns;jw1=nv;
% plist2 = sublist(ns,nv,'portrait');iw2=nv;jw2=ns; 
% ipl = 0;
% for iset = 1 : ns
%	for ivar = 1 : nv
%		ipl = ipl + 1;
%		figure(1);subplot(iw1,jw1,plist1(ipl));title(sprintf('Set:%i, Var:%i',iset,ivar));
%		figure(2);subplot(iw2,jw2,plist2(ipl));title(sprintf('Set:%i, Var:%i',iset,ivar));
%	end %for ivar
% end %for iset
%
% Created: 2009-08-06.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)