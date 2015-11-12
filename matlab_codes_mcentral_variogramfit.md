## variogramfit.m ##
Fit a theoretical variogram to an experimental variogram

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/variogramfit.m)

```
%variogramfit Fit a theoretical variogram to an experimental variogram
%
% Syntax:
%
%     [a,c,n] = variogramfit(h,gammaexp,a0,c0)
%     [a,c,n] = variogramfit(h,gammaexp,a0,c0,numobs)
%     [a,c,n] = variogramfit(h,gammaexp,a0,c0,numobs,'pn','pv',...)
%     [a,c,n,S] = variogramfit(...)
%
% Description:
%
%     variogramfit performs a least squares fit of various theoretical 
%     variograms to an experimental, isotropic variogram. The user can
%     choose between various bounded (e.g. spherical) and unbounded (e.g.
%     exponential) models. A nugget variance can be modelled as well, but
%     higher nested models are not supported.
%
%     The function works best with the function fminsearchbnd available on
%     the FEX. You should download it from the File Exchange (File ID:
%     #8277). If you don't have fminsearchbnd, variogramfit uses
%     fminsearch. The problem with fminsearch is, that it might return 
%     negative variances or ranges.
%
%     The variogram fitting algorithm is in particular sensitive to initial
%     values below the optimal solution. In case you have no idea of
%     initial values variogramfit calculates initial values for you
%     (c0 = max(gammaexp); a0 = max(h)*2/3;). If this is a reasonable
%     guess remains to be answered. Hence, visually inspecting your data
%     and estimating a theoretical variogram by hand should always be
%     your first choice.
%
%     Note that for unbounded models, the supplied parameter a0 (range) is
%     the distance where gamma equals 95% of the sill variance. The
%     returned parameter a0, however, is the parameter r in the model. The
%     range at 95% of the sill variance is then approximately 3*r.
%
% Input arguments:
%
%     h         lag distance of the experimental variogram
%     gammaexp  experimental variogram values (gamma)
%     a0        initial value (scalar) for range
%     c0        initial value (scalar) for sill variance
%     numobs    number of observations per lag distance (used for weight
%               function)
%
% Output arguments:
%
%     a         range
%     c         sill
%     n         nugget (empty if nugget variance is not applied)
%     S         structure array with additional information
%               .range
%               .sill
%               .nugget
%               .model - theoretical variogram
%               .func - anonymous function of variogram model (only the
%               function within range for bounded models)
%               .h  - distance
%               .gamma  - experimental variogram values
%               .gammahat - estimated variogram values
%               .residuals - residuals
%               .Rs - R-square of goodness of fit
%               .weights - weights
%               .exitflag - see fminsearch
%               .algorithm - see fminsearch
%               .funcCount - see fminsearch
%               .iterations - see fminsearch
%               .message - see fminsearch
%
% Property name/property values:
% 
%     'model'   a string that defines the function that can be fitted 
%               to the experimental variogram. 
% 
%               Supported bounded functions are:
%               'blinear' (bounded linear) 
%               'circular' (circular model)
%               'spherical' (spherical model, =default)
%               'pentaspherical' (pentaspherical model)
% 
%               Supported unbounded functions are:
%               'exponential' (exponential model)
%               'gaussian' (gaussian variogram)
%               'whittle' Whittle's elementary correlation (involves a
%                         modified Bessel function of the second kind.
%               'stable' (stable models sensu Wackernagel 1995). Same as
%                         gaussian, but with different exponents. Supply 
%                         the exponent alpha (<2) in an additional pn,pv 
%                         pair: 
%                        'stablealpha',alpha (default = 1.5).
%               'matern' Matern model. Requires an additional pn,pv pair. 
%                        'nu',nu (shape parameter > 0, default = 1)
%                        Note that for particular values of nu the matern 
%                        model reduces to other authorized variogram models.
%                        nu = 0.5 : exponential model
%                        nu = 1 : Whittles model
%                        nu -> inf : Gaussian model
%               
%               See Webster and Oliver (2001) for an overview on variogram 
%               models. See Minasny & McBratney (2005) for an introduction
%               to the Matern variogram.
%           
%     'nugget'  initial value (scalar) for nugget variance. The default
%               value is []. In this case variogramfit doesn't fit a nugget
%               variance. 
% 
%     'plotit'  true (default), false: plot experimental and theoretical 
%               variogram together.
% 
%     'solver'  'fminsearchbnd' (default) same as fminsearch , but with  
%               bound constraints by transformation (function by John 
%               D'Errico, File ID: #8277 on the FEX). The advantage in 
%               applying fminsearchbnd is that upper and lower bound 
%               constraints can be applied. That prevents that nugget 
%               variance or range may become negative.           
%               'fminsearch'
%
%     'weightfun' 'none' (default). 'cressie85' and 'mcbratney86' require
%               you to include the number of observations per experimental
%               gamma value (as returned by VARIOGRAM). 
%               'cressie85' uses m(hi)/gammahat(hi)^2 as weights
%               'mcbratney86' uses m(hi)*gammaexp(hi)/gammahat(hi)^3
%               
%
% Example: fit a variogram to experimental data
%
%     load variogramexample
%     a0 = 15; % initial value: range 
%     c0 = 0.1; % initial value: sill 
%     [a,c,n] = variogramfit(h,gammaexp,a0,c0,[],...
%                            'solver','fminsearchbnd',...
%                            'nugget',0,...
%                            'plotit',true);
%
%           
% See also: VARIOGRAM, FMINSEARCH, FMINSEARCHBND
%           
%
% References: Wackernagel, H. (1995): Multivariate Geostatistics, Springer.
%             Webster, R., Oliver, M. (2001): Geostatistics for
%             Environmental Scientists. Wiley & Sons.
%             Minsasny, B., McBratney, A. B. (2005): The Matrn function as
%             general model for soil variograms. Geoderma, 3-4, 192-207.
% 
% Date: 7. October, 2010
% Author: Wolfgang Schwanghart (w.schwanghart[at]unibas.ch)
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)