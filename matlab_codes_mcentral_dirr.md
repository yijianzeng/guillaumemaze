## DIRR.m ##
Lists all files in the current directory and sub directories recursively.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/dirr.m)

```
% DIRR Lists all files in the current directory and sub directories recursively.
% 
% [LIST] = DIRR(PATH)
% Returns a structure LIST with the same fieldnames as returned 
% by LIST = DIR(PATH)
% PATH can contain wildcards * and ? after the last \ or / (filename
% filter)
% The content of each directory in PATH is listed inside its 'isdir'
% field with the same format. The 'bytes' field is NOT zero but the
% sum of all filesizes inside the directory.
% 
% [LIST,BYTES] = DIRR(PATH)
% BYTES is a structure with fields 'total' and 'dir'. 'total' is the total
% size of PATH. 'dir' is a recursive substructure that contains the
% same fields ('total' and 'dir') for the subdirectories.
% 
% [...] = DIRR(PATH,FILTER)
% Lists only files matching the string FILTER (non case sensitive
% regular expression).
% N.B.: FILTER is optional and must not be equal to a fieldname
% ('name' or 'date' ... will never be interpreted as filters)
% 
% [LIST,BYTES,FIELDOUT] = DIRR(PATH,FIELDIN, ...)
% FIELDIN is a string specifying a field (of the structure LIST) that
% will be listed in a separate cell array of strings in FIELDOUT for
% every file with absolute path at the begining of the string.
% Multiple fields can be specified.
% 
% [LIST,BYTES,FIELDOUT] = DIRR(PATH,FIELDIN,FILTER, ...)
% Only files for which FIELDIN matches FILTER will be returned.
% Multiple [FIELDIN, FILTER] couples may be specified.
% Recursion can be avoided here by setting 'isdir' filter to '0'.
% For bytes, numeric comparison will be performed.
% 
% 
% EXAMPLES :
% 
% DIRR
% Lists all files (including path) in the current directory and it's
% subdirectories recursively.
% 
% DIRR('c:\matlab6p5\work\*.m')
% Lists all M-files in the c:\matlab6p5\work directory and it's
% subdirectories recursively.
% 
% Music = DIRR('G:\Ma musique\&Styles\Reggae\Alpha Blondy')
% Returns a structure Music very similar to what DIR returns 
% but containing the information on the files stored in
% subdirectories of 'G:\Ma musique\&Styles\Reggae\Alpha Blondy'.
% The structure Music is a bit difficult to explore though.
% See next examples.
% 
% [Files,Bytes,Names] = DIRR('c:\matlab6p5\toolbox','\.mex\>','name')
% Lists all MEX-files in the c:\matlab6p5\toolbox directory in the cell
% array of strings Names (including path).
% Note the regexp syntax of the filter string.
% Bytes is a structure with fields "total" and "dir". total is the
% total size of the directory, dir is a recursive substructure with
% the same fields as bytes for the subdirectories. 
% 
% [Files,Bytes,Names] = DIRR('c:\toto'...
%       ,'name','bytes','>50000','isdir','0')
% Lists all files larger than 50000 bytes NOT recursively.
% 
% [Files,Bytes,Dates] = DIRR('c:\matlab6p5\work','date','2005')
% Lists all dates of files from year 2005. (With path in front of
% date in the cell array of strings Dates)
% 
% 
% 
%       v1.02        
%       Maximilien Chaumon
%       maximilien.chaumon@chups.jussieu.fr
%       2006 06 16
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)