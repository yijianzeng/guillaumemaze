## chi2conf.m ##
Confidence interval using inverse of chi-square cdf.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/chi2conf.m)

```
% CHI2CONF Confidence interval using inverse of chi-square cdf.
%   C = CHI2CONF(P,K) is the confidence interval of an unbiased power spectrum 
%   estimate made up of K independent measurements.  C is a two element
%   vector.  We are P*100% confident that the true PSD lies in the interval
%   [C(1)*X C(2)*X], where X is the PSD estimate.
%
%   Reference:
%     Stephen Kay, "Modern Spectral Analysis, Theory & Application," 
%     p. 76, eqn 4.16.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)