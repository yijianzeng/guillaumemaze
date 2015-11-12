## taylordiag.m ##
Plot a Taylor Diagram

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/statistics/taylordiag.m)

```
% TAYLORDIAG Plot a Taylor Diagram
%
% [hp ht axl] = taylordiag(STDs,RMSs,CORs,['option',value])
%
% Plot a Taylor diagram from statistics of different series.
%
% INPUTS:
%	STDs: Standard deviations
%	RMSs: Centered Root Mean Square Difference 
%	CORs: Correlation
%
%	Each of these inputs are one dimensional with same length. First
%	indice corresponds to the reference serie for the diagram. For exemple
%	STDs(1) is the standard deviation of the reference serie and STDs(2:N) 
%	are the standard deviations of the other series.
% 
%	Note that by definition the following relation must be true for all series i:
%	RMSs(i) - sqrt(STDs(i).^2 + STDs(1)^2 - 2*STDs(i)*STDs(1).*CORs(i)) = 0
%	This relation is checked and if not verified an error message is sent. Please see
%	Taylor's JGR article for more informations about this.	
%	You can use the ALLSTATS function to avoid this to happen, I guess ;-). You can get
%
% OUTPUTS:
% 	hp: returns handles of plotted points
%	ht: returns handles of the text legend of points
%	axl: returns a structure of handles of axis labels
%
% LIST OF OPTIONS:
%	For an exhaustive list of options to customize your diagram, please call the function
%	without arguments:
%		>> taylordiag
%
% SHORT TUTORIAL (see taylordiag_test.m for more informations):
%	 An easy way to get compute inputs is to use the ALLSTATS function you can get from:
%	 Let's say you gathered all the series you want to put in the Taylor diagram in a 
%	 single matrix BUOY(N,nt) with N the number of series and nt their (similar) length.
%	 If BUOY(1,:) is the serie of reference for the diagram:
%		 for iserie = 2 : size(BUOY,1)
%		    S = allstats(BUOY(1,:),BUOY(iserie,:));
%		    MYSTATS(iserie,:) = S(:,2); % We get stats versus reference
%		 end%for iserie
%		 MYSTATS(1,:) = S(:,1); % We assign reference stats to the first row
%	 Note that the ALLSTATS function can handle NaNs, so be careful to compute statistics
%	 with enough points !
%	 Then you're ready to simply run:
%		taylordiag(MYSTATS(:,2),MYSTATS(:,3),MYSTATS(:,4));
%	
% REF: 	K. Taylor 
%		Summarizing multiple aspects of model performance in a single diagram
%		Journal of Geophysical Research-Atmospheres, 2001, V106, D7.
%
% Rev. by Guillaume Maze on 2010-02-10: Help more helpful ! Options now displayed by call.
% All rights reserved.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)