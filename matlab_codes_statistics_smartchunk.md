## smartchunk.m ##
Compute homogeneous chunks of data

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/smartchunk.m)

```
%smartchunk Compute homogeneous chunks of data
%
% [CHUNKS IDAT SCORE] = smartchunk(DATASET,NWORKER,[ARG,VAL])
% 
% Compute NWORKER homogeneous chunks of data from DATASET so that
% chunks can be dispatch to multiple workers/processes/jobs.
%
% Inputs:
% 	DATASET: is an 1D array of data to chunk
% 	NWORKER: is an integer defining the number of chunks to create
% 
% Options (defined with ARG/VAL pairs):
% 	metric: the function name to compute the metric to be homogeneized 
% 		among chunks. 'nansum' is the default value.
% 		Eg: smartchunk(DATASET,NWORKER,'metric','nanmean')
% 	niter: the optimization maximum number of iteration (1e4 by default)
% 		Eg: smartchunk(DATASET,NWORKER,'niter',5e4)
% 
% Outputs:
% 	CHUNKS: is a 2D array (NWORKER x CHUNKSIZE) with the chunk of DATASET
% 	IDAT: is a 2D array (NWORKER x CHUNKSIZE) with the indeces of DATASET used
% 		by CHUNKS: CHUNKS = DATASET(IDAT)
% 	SCORE: is the optimized minimum std among metrics of chunks.
% 
% Eg:
% 	Minimize the std along size(chunks,1) of the sum of chunks along size(chunks,2):
% 	[chunks, idat, score] = smartchunk([12 2 3 30 18 8],4)
% 
% 	This dataset is chunked into two peaces with equal sum of 10 (thus score = 0):
% 	[chunks, idat, score] = smartchunk([10 2 4 2 2],2)
% 	
% 
% Created: 2013-03-07.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)