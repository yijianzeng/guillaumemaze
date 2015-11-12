## myqst.m ##
Display qstat results

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/inout/myqst.m)

```
% MYQST Display qstat results
%
% [JOBLIST] = MYQST([ORDER])
% Display qstat results
%
% This function displays on a table the results of 'qstat -u <user>'
% ORDER indicates how to sort the results. It is a number designating
% of the output columns:
% 1 - ID 		: Job id
% 2 - Log		: This is the name of the job
% 3 - State		: State of the run (r:running, dr:scheduled for deletion, qw: waiting in the queue)
% 4 - Started	: Date of the job starting time
% 5 - Last touch: Date of the last modification of the output log file (DEFAULT SORTING COLUMN)
% 6 - Queue		: Name of the queue where the job is running
% The sorting column is indicated by a (*) mark.
%
% Created by Guillaume Maze on 2008-10-28.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)