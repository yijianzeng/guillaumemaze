## clusterData.m ##
Clusters an MxN array of data into an unspecified number (P) of bins.

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/mcentral/clusterData.m)

```
% Clusters an MxN array of data into an unspecified number (P) of bins.
%
% No a priori knowledge of the number of bins, or the distance between
% bins, is required. This approach relies on the relative difference
% between (sorted) elements of the data, and works well when the difference
% between clusters is bigger than the difference between elements
% within a cluster.
%
% SYNTAX:
% CLUSTERS = CLUSTERDATA(DATA);
%            Clusters an MxN matrix of data (DATA)
%            COLUMN-BY-COLUMN, and returns a cell array of the
%            individual clusters. Each column may have a
%            different interpretation. For instance, an Mx4
%            array of data may represent x-data in the first
%            column, y- in the second, z- in the third, and
%            t- in the fourth. Returns a Px1 cell array,
%            CLUSTERS, specifying the data points in each
%            of the P clusters detected.
%
% CLUSTERS = CLUSTERDATA(DATA, SENSITIVITY);
%            Optional input argument SENSITIVITY allows you
%            to adjust the "difference sensitivity" between
%            clusters. Sensitivity should be provided as a
%            normalized value on [0,1]. Sensitivity may be
%            either: EMPTY: default value (0.2) will be used
%            for each columnwise clustering; A SCALAR:
%            sensitivity value will be uniformly applied for
%            each columnwise clustering; A 1xN (or Nx1)
%            VECTOR of sensitivities, applied elementwise to
%            the columnwise clustering. With a higher
%            sensitivity, expect fewer clusters; with a lower
%            sensitivity, more clusters. (DEFAULT: 0.2;
%            indicates that clusters should be separated by
%            at least 20% of the distance separating the two
%            most widely separated data points.)
% 
% [...,CLUSTERINDS] = CLUSTERDATA(...);
%            Also returns an Mx1 vector of the cluster
%            indices of each data point (row).
%
% [...,...,CLUSTERBOUNDS] = CLUSTERDATA(...);
%            Also returns in a 1xN cell array the lower and
%            upper limits for each column that separate the
%            data into their clustered bins.
%
% EXAMPLES:
%
% % Example 1: 
%
% a = [1 1 1; 1 2 1; 10 10 10; 11 11 11; 30 11 10; 29 10 1];
% scatter3(a(:,1),a(:,2),a(:,3),'b.');
% set(gca,'color',[0.3 0.3 0.3])
% xlabel('x');ylabel('y');zlabel('z');
%
% [clusters,clusterInds,clusterBounds] = clusterData(a);
% colors = jet(numel(clusters));
% %Now display the results:
% hold on
% for ii = 1:numel(clusters)
% plot3(clusters{ii}(:,1),clusters{ii}(:,2),clusters{ii}(:,3),...
%    'linestyle','none','linewidth',3,'marker','o','color',colors(ii,:));
% end
%
% % Example 2: Create a random number of groups of data, each with a
% %            random number of points, and separate them into clusters.
%
% nClusters = randi(50);
% maxAbs = 1000; spread = 75;
% maxPointsPerCluster = randi(300);
% xyz = [];
% for ii = 1:nClusters
%     clusterPoints = randi(maxPointsPerCluster);
%     xyz = [xyz;...
%         bsxfun(@plus,randi(maxAbs,[1,3]),spread*rand([clusterPoints,3]))];
% end
% figure;
% scatter3(xyz(:,1),xyz(:,2),xyz(:,3),'b.')
% xlabel('x');ylabel('y');zlabel('z');
% 
% [clusters,clusterInds,clusterBounds] = clusterData(xyz);
% colors = jet(numel(clusters));
% inds = randperm(numel(clusters));
% colors = colors(inds,:);
% figure;
% scatter3(xyz(:,1),xyz(:,2),xyz(:,3),'b.')
% xlabel('x');ylabel('y');zlabel('z');
% hold on
% for ii = 1:numel(clusters)
% plot3(clusters{ii}(:,1),clusters{ii}(:,2),clusters{ii}(:,3),...
%     'linestyle','none','linewidth',2,'marker','o','color',colors(ii,:));
% end
% 
% % Example 3: Using the data created in example 2,
%              recluster the data using a vector of
%              non-default sensitivity values:
%
% [clusters,clusterInds,clusterBounds] =...
% clusterData(xyz,[0.25 0.4 0.2]);
%
% NOTE: clusterData replaces an earlier implementation
% called "ezCluster," which operated  only on a vector of
% data.
%
% Written by Brett Shoelson, PhD
% 06/12/2010; 02/08/2012
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)