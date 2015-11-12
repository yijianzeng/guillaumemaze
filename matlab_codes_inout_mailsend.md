## mailsend.m ##
Send an email via the system command 'mail'

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/mailsend.m)

```
% MAILSEND Send an email via the system command 'mail'
%
% [] = mailsend(email,subject,'body string')           % Use a string
% [] = mailsend(email,subject,'body line1 \nline 2')   % Use \n in string to add new lines
% [] = mailsend(email,subject,{'body line1','line 2'}) % Use cell array of strings
% [] = mailsend(email,subject,{'body line1',132})      % Use cell array of strings or not
% [] = mailsend(email,subject,'body_file_content.txt') % Use a text file content 
%
% Send an email via the system command 'mail'
%
% Created by Guillaume Maze on 2008-10-14.
% Revised: 2014-04-30 (G. Maze) Added support for file content in the body
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)