## ltp.m ##
List directory as ls -rtl

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/ltp.m)

```
% ltp List directory as ls -rtl
%
% [] = ltp([dir])
% 
%   LTP displays the results of the 'ls -rtl' command on UNIX. On UNIX, 
%   LTP returns a character row vector of filenames separated 
%   by tab and space characters. On Windows, LTP returns an m-by-n 
%   character array of filenames, where m is the number of filenames 
%   and n is the number of characters in the longest filename found. 
%   Filenames shorter than n characters are padded with space characters.
%
%   You can pass any flags to LTP as well that your operating system supports.
%
%   See also DIR, MKDIR, RMDIR, FILEATTRIB, COPYFILE, MOVEFILE, DELETE.
%
%
% Created: 2009-07-20.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)