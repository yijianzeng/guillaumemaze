## kriging.m ##
Interpolation with ordinary kriging in two dimensions

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/kriging.m)

```
%kriging Interpolation with ordinary kriging in two dimensions
%
% Syntax:
%
%     [zi,zivar] = kriging(vstruct,x,y,z,xi,yi)
%     [zi,zivar] = kriging(vstruct,x,y,z,xi,yi,chunksize)
%
% Description:
%
%     kriging uses ordinary kriging to interpolate a variable z measured at
%     locations with the coordinates x and y at unsampled locations xi, yi.
%     The function requires the variable vstruct that contains all
%     necessary information on the variogram. vstruct is the forth output
%     argument of the function variogramfit.
%
%     This is a rudimentary, but easy to use function to perform a simple
%     kriging interpolation. I call it rudimentary since it always includes
%     ALL observations to estimate values at unsampled locations. This may
%     not be necessary when sample locations are not within the
%     autocorrelation range but would require something like a k nearest
%     neighbor search algorithm or something similar. Thus, the algorithms
%     works best for relatively small numbers of observations (100-500).
%     For larger numbers of observations I recommend the use of GSTAT.
%
%     Note that kriging fails if there are two or more observations at one
%     location or very, very close to each other. This may cause that the 
%     system of equation is badly conditioned. Currently, I use the
%     pseudo-inverse (pinv) to come around this problem. If you have better
%     ideas, please let me know.
%
% Input arguments:
%
%     vstruct   structure array with variogram information as returned
%               variogramfit (forth output argument)
%     x,y       coordinates of observations
%     z         values of observations
%     xi,yi     coordinates of locations for predictions 
%     chunksize nr of elements in zi that are processed at one time.
%               The default is 100, but this depends largely on your 
%               available main memory and numel(x).
%
% Output arguments:
%
%     zi        kriging predictions
%     zivar     kriging variance
%
% Example:
%
%     % create random field with autocorrelation
%     [X,Y] = meshgrid(0:500);
%     Z = randn(size(X));
%     Z = imfilter(Z,fspecial('gaussian',[40 40],8));
%
%     % sample the field
%     n = 500;
%     x = rand(n,1)*500;
%     y = rand(n,1)*500;
%     z = interp2(X,Y,Z,x,y);
%
%     % plot the random field
%     subplot(2,2,1)
%     imagesc(X(1,:),Y(:,1),Z); axis image; axis xy
%     hold on
%     plot(x,y,'.k')
%     title('random field with sampling locations')
%
%     % calculate the sample variogram
%     v = variogram([x y],z,'plotit',false,'maxdist',100);
%     % and fit a spherical variogram
%     subplot(2,2,2)
%     [dum,dum,dum,vstruct] = variogramfit(v.distance,v.val,[],[],[],'model','stable');
%     title('variogram')
%
%     % now use the sampled locations in a kriging
%     [Zhat,Zvar] = kriging(vstruct,x,y,z,X,Y);
%     subplot(2,2,3)
%     imagesc(X(1,:),Y(:,1),Zhat); axis image; axis xy
%     title('kriging predictions')
%     subplot(2,2,4)
%     contour(X,Y,Zvar); axis image
%     title('kriging variance')
%
%
% see also: variogram, variogramfit, consolidator, pinv
%
% Date: 13. October, 2010
% Author: Wolfgang Schwanghart (w.schwanghart[at]unibas.ch)
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)