## simplify\_unit.m ##
Simplify unit expression

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/simplify_unit.m)

```
% simplify_unit Simplify unit expression
%
% U = simplify_unit(U,[VERB])
% 
% Simplify unit expression U.
% U is a string with products and ratios of units 
% such like: 'm^2/s'
% Option VERB set to 1/true will print some infomations on
% screen.
% 
% Remarks:
%	Powers can be handled if between (.)
% 	Blank spaces are considered as products 'a b' = 'a*b'
% 	Anything between '*' and '/' is considered as a unit.
% 	The function is case sensitive.
%
% Example:
%	simplify_unit('m^2/s*s') % will return: 'm^2'
%	simplify_unit('m^2/s*m^(3/2)') % will return: 'm^(7/2)/s'
%	simplify_unit('1/10^4 1/10^6 mol/kg kg/m^3 m ') % will return: '1/10^10/m^2*mol'
%
% Be careful with LaTeX notations:
%	simplify_unit('\mu mol/kg * kg')
% will return: '\mu*mol'
% while
%	simplify_unit('\mumol/kg * kg')
% will return: '\mumol' as expected
% However, 
%	simplify_unit('^oC/kg * kg')
%	simplify_unit('m^{-3}/kg * kg')
% will return errors. Reformat your string or use (.) for numerical powers
%
% Created: 2010-11-17
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)