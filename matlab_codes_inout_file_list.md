## file\_list.m ##
Create a file list from a folder

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/file_list.m)

```
% file_list Create a file list from a folder
%
% FLIST = file_list(FOLDER_PARENT,[OPTION1,VALUE1,...]);
% 
% Inputs:
%	FOLDER_PARENT (string): path to the folder to scan
%
% Options:
%	WFILE (double): 1 to backup all files, 0 to backup files with known extensions (defined in get_list_ext_ok);
%	NREC (double): depth of the recursive loop into folders (any integer or Inf)
%	EXTE (cell of strings): File extensions to select
%
% Output:
%	FLIST is a cell array:
%	FLIST{:,1}: Complete path to the file
%	FLIST{:,2}: File name
%	FLIST{:,3}: Size (bytes)
%	FLIST{:,4}: Folder to the file
%	FLIST{:,5}: Modification date as a Matlab serial number
%
% Created: 2009-09-25.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)