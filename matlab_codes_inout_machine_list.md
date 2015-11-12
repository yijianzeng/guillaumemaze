## machine\_list.m ##
List all network machine with system command 'nslookup'

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/machine_list.m)

```
% machine_list List all network machine with system command 'nslookup'
%
% [] = machine_list(DOMAIN)
% 
% From: nslookup DOMAIN, iterates on the III = 1:255 ip
% of XXX.XXX.III to get the list of machine's names available.
% No ping is done, so no informations about the machine's
% status is provided.
% The machine list is written in the text file:
% 	~/matlab/routines/data/machine_list_DOMAIN.txt
%
%
% Created: 2009-08-19.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)