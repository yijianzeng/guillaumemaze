## dispt.m ##
Display a table on prompt

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/matrix/dispt.m)

```
% dispt Display a table on prompt
%
% [LINES] = dispt(C,[OPTIONS]);
% 
% Custom matrix display on prompt of double matrix C.
%
% OPTIONS are paired like: OPTION_NAME,OPTION_VALUE
%
% List of OPTIONS:
%	numform (string): Numerical format use to display values of C.
%		Default value: %0.2f
%	rowT: Title of rows to appear in the upper left table.
%	colT: Title of columns to appear in the upper left table.
%	rowl: Row labels.
%	coll: Column labels.
%		About rowl and coll:
%			They can a string with a char for each column or row.
%			They can a single char, in this case the rol/col number is added
%			They can a cell of one string with the ley '#r' replaced by 
%				the rol/col number
%			Or they can be a cell of strings for each column or row.
%	dohline (logical): Insert a horizontal line between each row.
%		Default value: false
%	col1w (integer): Width of the first column.
%		Default value: 12
%	colw (integer): Width of each columns.
%		Default value: 10
%
% Outputs:
%	LINES is a cell with each lines displayed on prompt as a row.
%
% Examples:
%	dispt(randn(4,6),'numform','%0.3f')
%	dispt(randn(4,6),'colT','Columns','rowT','Rows')
%	dispt(randn(4,6),'colT','Columns','rowT','Rows','col1w',20)
%	dispt(randn(4,6),'coll','abcdef')
%	dispt(randn(4,6),'coll',{'Column number #r'})
%	dispt(randn(4,3),'coll',{'Column number #r'},'rowl',{'Row number #r'},'colw',20,'col1w',20)
%
% Created: 2010-06-10.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)