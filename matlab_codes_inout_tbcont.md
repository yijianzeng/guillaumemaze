## tbcont.m ##
Audit a directory and create html/wiki pages and a table of content

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/tbcont.m)

```
% TBCONT Audit a directory and create html/wiki pages and a table of content
%
% [] = tbcont(PATH_TO_DIR,[OPTION1,VALUE1,...])
%
% Scan the directory PATH_TO_DIR and create html/wiki pages and table of content for
% matlab script files (*.m).
%
% The function creates under PATH_TO_DIR:
% 	- a tbcont.html file with an index of all .m routines
%		This is not a standlone html file because it has no header and body.
%		It contains a html table to be inserted in any webpage. However, 
%		most modern browsers will support this and display the content.
%	- a 'help' folder with html help file for each routines
%	- a 'wiki' folder with wiki help file for each routines
%	- a Contents.m file with an index of all .m routines
%
% OPTIONS:
%	link_pref (string): Absolute base path to source .m files
%		By default: 'http://guillaumemaze.googlecode.com/svn/trunk/matlab/'
%	link_rel (string): relative path to source .m files from link_pref
%		So that url to source file is: link_pref/link_rel/XXXX.m
%	link_wiki (string): Absolute path to wiki pages
%		By default: 'http://code.google.com/p/guillaumemaze/wiki'
%		All wiki pages are under the same directory PATH_TO_DIR/wiki/
%		Unlike html pages, no subfolders are created.
%	ndepth (integer): Depth of the recursive scan of folders
%		0 means only PATH_TO_DIR/*.m files will be incorporated
%		1 means only PATH_TO_DIR/*.m and PATH_TO_DIR/*/*.m files will be incorporated
%		etc
%		if ndpeth > 0, then url to source file is: link_pref/link_rel/SUBFOLDER/XXXX.m, etc ...
%
% TBCONT.HTML FILE DESCRIPTION:
% 	In tbcont.html, we create a first table 'Quick Links' which 
% 	lists all routines and link them to an url of the source file. 
% 	The url prefix for these links is by default relative to:
%		'http://guillaumemaze.googlecode.com/svn/trunk/matlab/';
% 	and it can be specified in the options list with opts link_rel.
%
% 	Then a second table lists all routines with there h1line as:
%		column 1: link to a wiki page for the routine
%		column 2: the h1line
%		column 3: link to the source file (similar to the one in the 'Quick Links' table)
%
% NOTES:
% - This function aims to be used in tight conjunction with a Google Code project svn repository.
% - If you want to have a clean TOC in Matlab, use function packver to manage packages versions
%
% EXAMPLE:
% Imagine there's one function called toto0.m under PATH_TO_DIR and one function called toto1.m
% under PATH_TO_DIR/test/
%	tbcont(PATH_TO_DIR,'link_rel',myexample);
% will create:
%	PATH_TO_DIR/tbcont.html
%	PATH_TO_DIR/Contents.m
%	PATH_TO_DIR/html/toto0.html
%	PATH_TO_DIR/html/test/toto1.html
%	PATH_TO_DIR/wiki/matlab_myexample_toto0.wiki
%	PATH_TO_DIR/wiki/matlab_myexample_test_toto1.wiki
% and links to source files points to:
%	http://guillaumemaze.googlecode.com/svn/trunk/matlab/myexample/toto0.m
%	http://guillaumemaze.googlecode.com/svn/trunk/matlab/myexample/test/toto1.m
% and links to wiki pages points to:
%	http://code.google.com/p/guillaumemaze/wiki/matlab_myexample_toto0
%	http://code.google.com/p/guillaumemaze/wiki/matlab_myexample_test_toto1
%
% 
% REQUIREMENTS:
%	Matlab function file_list()
%
% Created: 2008-10-30.
% Rev. by Guillaume Maze on 2009-09-28: Added Contents.m creation, ndepth option
% Rev. by Guillaume Maze on 2009-09-25: Added complete help, Handle options, Manage subfolders
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)