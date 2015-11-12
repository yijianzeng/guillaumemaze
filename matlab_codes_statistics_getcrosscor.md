## getcrosscor.m ##
Compute a lagged cross-correlation

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/getcrosscor.m)

```
% GETCROSSCOR Compute a lagged cross-correlation 
%
% [CR LAGS CONFIDENCE95 PROB] = GETCROSSCOR(X1,X2,T)
% 
% Compute the cross-correlation between X1 and X2
% with lags from -T to T
%
%     CR(find(PROB>0.05)) = ones(1,length(find(PROB>0.05))).*NaN;
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)