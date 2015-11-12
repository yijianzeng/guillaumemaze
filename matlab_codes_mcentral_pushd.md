## pushd.m ##
Changes MATLAB working directory to the one specified, or to the folder containing the specified file

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/pushd.m)

```
%PUSHD  Changes MATLAB working directory to the one specified, or to the folder containing the specified file
%   PUSHD(directory/file) stores the current working directory and changes current directory to the one 
%   specified in the string directory/file.  Files must exist in the MATLAB path. To get back to the stored
%   directory call POPD, see help popd.
%   
%   PUSHD(directory) changes working dir to to the directory specified in
%   the string directory. 
%
%   PUSHD(file) changes the directory to the one containing file. The file
%   has to be in the MATLAB path.
%   
%   PUSHD without argument stores MATLAB current directory
%
%   
%   Example 1:          Directories
%   pushd('..\');       % Move to one step up in the folder hierarchy and store current directory
%   pwd                 % Check current dir
%   popd;               % Use popd to get back to the stored directory
%   pwd                 % Check current dir
%   
%   Example 2:          Files
%   pushd('sin');       % Move to the folder containing sin.m
%   pwd                 % Check current dir
%
%   Example 3:          Non-functional calls
%   pushd ..\..\        % Moves two steps, using non-functional call 
%   pwd
%  
%   Example 4:          Stack pushing
%   pushd ..\..
%   % do something
%   pushd filter
%   pwd
%   % do something else
%   popd                % Now you are in ..\..
%   pwd
%   popd                % Now you are back where you started
%   pwd
%
%   Example 5:
%   pushd dirspec       % dirspec can be any directory in your matlab-path
% 
% 
% 
%   See also popd, cd, pwd
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)