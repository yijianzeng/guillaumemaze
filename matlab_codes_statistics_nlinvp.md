## nlinvp.m ##
Non-Linear inverse problem

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/nlinvp.m)

```
% nlinvp  Non-Linear inverse problem
%
% [Xs, Cs, FXs, FX0] = nlinvp(X0,C0,F,CT,F0,[OPTIONS])
% 
% Solve a non-linear inverse problem.
%
% Given f a set of constraints to be applied at points X
% F is the matrix of partial derivatives of f with respect to X:
%	F(t,k) = d f(t) / d X(k)
% Because the problem is non-linear, any X(k) can be found in F(t,k)
%
% With:	
% 	NC the Number of constraints and
% 	NU the Number of unknowns to be estimated,
%
% INPUTS:
%	X0: A priori unknowns estimates
%		size(X0) = NU x 1
%	C0: A priori error covariance matrix of unknowns estimates
%		size(C0) = NU x NU
%	F: Constraints matrix
%		size(F) = NC x NU
% 	CT: A priori error covariance matrix on constraints
%		size(CT) = NC x NC
% 	F0: a priori constraints estimate -> f(X0)
%		size(F0) = NC x 1
%
% OUTPUTS:
% 	Xs: unknowns estimates
%		size(Xs) = NU x 1	
% 	Cs: error covariance matrix of unknowns estimates
%		size(Cs) = NU x NU
% 	FXs = F*Xs-F0: A posteriori constraints residuals
%		size(FXs) = NC x 1
% 	FX0 = F*X0-F0 : A priori constraints residuals
%		size(FX0) = NC x 1
%
% Ref: 
%	A.Tarantola and B.Valette. Generalized nonlinear inverse problems 
%		solved using the least squares criterion. 
%		Rev. Geophys. Space Phys, 20(2):219232, 1982.
% 	H.Mercier. Determining the general circulation of the ocean: A 
%		nonlinear inverse problem. J. Geophys. Res., 91(C4):51035109, 1986.
%		http://dx.doi.org/10.1029/JC091iC04p05103
%
% See Also:
%	linvp
%
% Created: 2010-09-09.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)