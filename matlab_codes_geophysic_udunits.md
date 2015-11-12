## udunits.m ##
Unidata units library

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/udunits.m)

```
% udunits Unidata units library
%
% [INFO] = udunits(UNIT)
% 
% Standard units definitions for Unidata softwares (netcdf...) 
%
% Input:
%	UNIT is a string to look for in the database units name.
%		It is case sensitive.
%
% Output:
%	INFO is a cell of structure with fields:
%		name: Unit name
%		plural: indicates whether or not the unit name has a plural 
%			form (i.e. with an 's' appended). A 'P' indicates that 
%			the unit has a plural form, whereas, a 'S' indicates
%			that the unit has a singular form only.
%		definition: Definition for the unit.
%		comment: Any comment from the original database file
%
% Source:
%	Id: udunits.dat,v 1.18 2006/09/20 18:59:18 steve Exp $
%	http://www.unidata.ucar.edu/software/udunits/
%
% Created: 2009-09-10.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)