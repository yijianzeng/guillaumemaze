## outliers.m ##
function: Remove outliers based on Thompson Tau:

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/outliers.m)

```
%outliers function: Remove outliers based on Thompson Tau:
% Summary: outliers are detected using Thompson Tau method and turned to 
% NaN in the output.
%
% Function Decription: 
% This function accepts a vector or matrix and detects the outlier values
% in the vector/matrix using Thopson Tau method, which is based on the
% absolute deviation of each record from the mean of the entire
% vector/matrix, and fills the outliers with NaNs in the returned output.
% The magnitude of Thompson's Tau value corresponding to the number of
% records in the input vector (m) or matrix (m*n) to the Standard Deviation
% of the input vector/matrix is the rule to decide if any record is in the
% outliers. The mean, standard deviation (std) and the magnitude of
% Thompson's Tau (tau*std) are calculated again after removal of each
% outlier. If the input is matrix, it will be converted to a vector before
% detecting the outliers, however, the output will be a matrix with the
% same m*n dimensions as input. Indexes of the outleirs also will be returned, where
% if the input was a vector, the index vector also will be a vector,
% however, if the input was a matrix, outlier indexes will be returned in a
% two-column matrix showing i,j indexes of the outliers (see examples below).
%
% --Inputs:
%   X0: input vector or matrix which contains outleirs
%   num_outliers: number of outliers that should be removed from the input
%   vector/matrix
%   
% --Outputs:
%   X: output vector/matrix with outliers (if any detected) turned to NaN 
%   outliers_idx: the index(es) of any detected outliers, the more extreme 
%   outliers will be detected first, so the first index refers to the 
%   most extreme outlier and so forth 
%
% --Theory of Thompson Tau method: 
%   http://www.mne.psu.edu/me345/Lectures/Outliers.pdf
%   http://www.jstor.org/stable/2345543 (Thompson, 1985)
%
% --Note: this function is an improvement based on Vince Petaccio, 2009:
% http://www.mathworks.com/matlabcentral/fileexchange/24885-remove-outliers
% --Improvements: 
%  1. Handleing NaNs in inputs
%  2. Number of outliers to be removed is restricted to a user defined
%  maximum to avoid uncontrolled shrinking of input dataset
%  3. Filling outliers by NaNs to preserve original dimensions of the input 
%  vector/matrix; this is crucial when the input variable is supposed to be
%  used with another variable with the same size (e.g., for plotting,
%  regression calculations, etc.)
%  4. Indexes of the outliers that have been detected and removed are
%  returned so that the user knows which records have been removed, and
%  since the indexes are ordered from the most extreme (negative or
%  positive) to less extreme outliers, user will know which point was in
%  the farthest outliers. 
%  5. Syntax and algorithm has been siginificantly improved, this includes
%  the logic for detection of the outliers from the upper and lower limits.
%  Logic to detect an outlier is solely based on the absolute distance of
%  each record from the central point rather than detecting the outliers
%  sequentially, which was the case in Vince Petaccio, 2009, where outliers
%  were detected and removed by order of one from the upper and the next
%  from the lower extremes. This code first arranges the extreme values
%  (upper or lower) to one side of the sorted vector based on the absolute
%  distance from the center (while preserving the original arrangment in
%  the input vector) then removes the bottom line element if it meets
%  outlier conditions. This process continues until num_outliers is
%  reached.
%  6. This function is enhanced to handle both vectors and matrices.
%
% --Examples:
% -Example 1. Vector input:
%  X0=[2.0, 3.0, -50.5, 4.0, 109.0, 6.0]
%  [X, outliers_idx] = outliers(X0, 2) %call function with vector input
%
%  X = 
%      2     3   NaN     4   NaN     6
% 
%  outliers_idx = 
%      5     3
% 
% -Example 2. Matrix input:
%  X0= [2.0,   3.0,   -50.5,    4.0,  109.0,   6.0;
%      5.3,   7.0,    80.0,    2.0,   NaN,    1.0;
%      5.1,   2.7,     3.8,    2.0,   3.5,    21.0]
%  [X, outliers_idx] = outliers(X0, 4) %call function with matrix input
% 
%  X =
%      2       3       NaN     4     NaN     6
%      5.3     7       NaN     2     NaN     1
%      5.1     2.7     3.8     2     3.5     NaN
%      
%  outliers_idx =
%    %(i)   (J)    %annotated 
%      1     5
%      2     3
%      1     3
%      3     6
%
% First version: 06 June 2012
% Enhanced to handle matrix: 09 June 2012
% email: sohrabinia.m@gmail.com
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)