## newclim.m ##
Used to get more than 1 colormap in subplot windows

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/colors/newclim.m)

```
% NEWCLIM Used to get more than 1 colormap in subplot windows
%
% CLim = newclim(BeginSlot,EndSlot,CDmin,CDmax,CmLength)
%                Convert slot number and range
%                to percent of colormap
% Used to get more than 1 colormap in subplot windows.
% 
% For example:
%
% z = peaks(25);
% map1=jet;
% map2=hot;
% ax1=subplot(1,2,1)
% imagesc(z);title('Colormap: jet');
% ax2=subplot(1,2,2)
% imagesc(z);title('Colormap: hot');
% colormap([map1;map2]);
%
% CmLength   = size(get(gcf,'Colormap'),1);% Colormap length
% BeginSlot1 = 1;          % Begining slot
% EndSlot1   = size(map1,1); % Ending slot
% BeginSlot2 = EndSlot1+1; 
% EndSlot2   = CmLength;
% CLim1      = get(ax1,'CLim');% CLim values for each axis
% CLim2      = get(ax2,'CLim');
% set(ax1,'CLim',newclim(BeginSlot1,EndSlot1,CLim1(1),CLim1(2),CmLength ))
% set(ax2,'CLim',newclim(BeginSlot2,EndSlot2,CLim2(1),CLim2(2),CmLength ))
%
%
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)