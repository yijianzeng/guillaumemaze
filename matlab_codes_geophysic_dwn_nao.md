## dwn\_nao.m ##
Download the monthly NAO index

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/dwn_nao.m)

```
% dwn_nao Download the monthly NAO index
%
% [NAO_index, NAO_time] = dwn_nao([DT])
% 
% Download the monthly NAO index at:
% http://www.cpc.noaa.gov/products/precip/CWlink/pna/norm.nao.monthly.b5001.current.ascii
%
% Inputs:
%	DT is the time step of the time serie
%		By default it is set to 'm' for monthly values
%		It can be:
%			'y' for yearly means
%			'w' for yearly winter values (DJFM average)
%
% Outputs:
%	NAO_index: well, the NAO index !
%	NAO_time: the time axis as returned by datenum
%
% Rq: The downloaded file is stored in ~/matlab/routines/data subdirectory
%
% Created: 2009-05-29.
% Rev. by Guillaume Maze on 2009-09-01: Add winter value option
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)