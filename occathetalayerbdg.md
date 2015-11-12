# Isothermal layers volume budget with OCCA #

## Introduction ##

This is a set of matlab and fortran routines to compute a thermally defined layer volume budget over a subdomain of the global ocean from the OCCA state estimate.

This package was developed by Guillaume Maze and Gael Forget at MIT (Cambridge, USA) for the ECCO group and the CLIMODE project.

You can browse it here:
http://code.google.com/p/guillaumemaze/source/browse/trunk/OCCA/Tlayer_budget

## Requirements ##

To perform this analysis you'll need:
  * From the OCCA state estimate release 0 or 1 the fields:
| **File name** | **Z levels** | **Grid** | **Unit** | **Definition** |
|:--------------|:-------------|:---------|:---------|:---------------|
| THETA         | 50           |SM        |degC            |Potential Temperature|
| TENDT         | 50           |SM        |degC/d          |Tendency of Potential Temperature|
| ZADVT         | 51           |WM        |degC.m^3/s      |Vertical   Advective Flux of Pot.Temp|
| XADVT         | 50           |UU        |degC.m^3/s      |Zonal      Advective Flux of Pot.Temp|
| YADVT         | 50           |VV        |degC.m^3/s      |Meridional Advective Flux of Pot.Temp|
| XDIFT         | 51           |WM        |degC.m^3/s      |Vertical   Diffusive Flux of Pot.Temp (Explicit part)|
| ZDIFTI        | 51           |WM        |degC.m^3/s      |Vertical   Diffusive Flux of Pot.Temp (Implicit part)|
| XDIFT         | 50           |UU        |degC.m^3/s      |Zonal      Diffusive Flux of Pot.Temp|
| YDIFT         | 50           |VV        |degC.m^3/s      |Meridional Diffusive Flux of Pot.Temp|
| GTABT         | 50           |SM        |degC/s          | Tendency of Potential Temp. added by the Adams Bashforth Scheme|
| GTFT          | 50           |SM        |degC/s          | Tendency of Potential Temp. due to air-sea heat fluxes|
| GHATT         | 51           |WM        |degC.m^3/s      | Non-local transport term of KPP as a temperature flux|
| DSSHT         | 51           |WM        |degC.m^3/s      | Vertical flux of Pot.temp due to Sea Level Change|

> These are normally defined on a 360x160x50 grid points, daily from 2003/11/1 to 2006/11/3 (1099 days). You can download OCCA here: http://www.ecco-group.org/products.htm or email Gael Forget.

  * All the grid files of OCCA.

  * This package. To download it, go to your working directory and type:

> `svn checkout http://guillaumemaze.googlecode.com/svn/trunk/OCCA/Tlayer_budget Tlayer_budget`


## Help ##

There are 2 steps in the computation. Step 1 extracts a subdomain of the Atlas, Step 2 computes the budget with a 3D interpolation of all fields.

### Step 1 ###
  * Into **Tlayer\_budget/step1** you have to tune the header of the function **extract\_subdomain.m** to match your environment.
> Variables that need to be tuned are:
    * **pathi**: this is where we find input fields (original theta and flux of temp. fields)
    * **patho**: this is where we print out fields restricted to the subdomain.
    * **subdomain**: this table defines the subdomain. It has the format:`[ixWest ixEast iySouth iyNorth izTop izBottom]`. For example: `subdomain = [122 200 90 130 1 25];` extract the Kuroshio region.
> You may want to tune the subfunction **wherearewe** to match your machine. You may also want to use a special mask for your domain of analysis. You can do so by looking at the subfunction **extract**. Finally, if you have a fancy OCCA dataset, you may have to tune how the routine name the input files. Check at variables **prefi**, **suffi** and the subfunction **open\_files**.
> Last, the function **extract\_subdomain.m** takes as an argument a number which correspond to a particular set of fields to extract:
| **Argument** | **Fields processed** |
|:-------------|:---------------------|
| 1            | Theta and volume elements|
| 2            | Tendency Native      |
| 3            | Tendency Artificial  |
| 4            | Air-sea heat flux    |
| 5            | All other terms (ssh, gtabt, ghatt)|
| 6            | Total and individual advection terms|
| 7            | Total and individual diffusion terms|

  * The routine **create\_queue\_scripts.m** create a set of script files to submit the function to a SGE queuing system. It also create a shell script to submit all in one command. What you have to tune in **create\_queue\_scripts.m** are the variables: **workdir** (this is where the **extract\_subdomain.m** routine is located) and **matlabpath** (this is where the job has to look for to find Matlab).


### Step 2 ###

  * Under **Tlayer\_budget/step2**, you first have to create a set of time line files to indicate the fortran routine when you want the budget to be computed (the full time serie, only januaries, etc ...). This is done with the **create\_timeline.m** routine where you only have to tune the variable **patho** to indicate where the time line files will be created.


  * Next, you have to create the parameters files for the fortran code with: **create\_param\_files.m**. There are several variables to be tuned here:
    * **patho**: This is where we print the param files
    * **homedir**: This is what we replace with the ~ into paths in order to deal with absolute paths.
    * **tmp\_path**: This is where the fortan code will print out the results
    * **lrf\_path**: This is where the fortran code looks for input fields (coming from step 1)
    * **time\_path**: This is where the fortran code looks for the time line.
> Then you have to select parameters for **klist** and **tlist** variables. They select what are the field(s) you want to compute the budget of and the time lines to use.
> > The variable **klist** can contain one of the following:
| **klist** | **Subdomain file analysed** (default name) |
|:----------|:-------------------------------------------|
| 1         | LRvol.3yV2adv.bin                          |
| 2         | LRtheta.3yV2adv.bin (NOT OK !)             |
| 3         | LRadvTOT.3yV2adv.bin                       |
| 4         | LRdiffTOT.3yV2adv.bin                      |
| 5         | LRairsea3D.3yV2adv.bin                     |
| 6         | LRtendNATIVE.3yV2adv.bin                   |
| 7         | LRtendARTIF.3yV2adv.bin                    |
| 8         | LRallotherTOT.3yV2adv.bin                  |
| 9         | LRadvX.3yV2adv.bin                         |
|10         | LRadvY.3yV2adv.bin                         |
|11         | LRadvZ.3yV2adv.bin                         |
|12         | LRdifX.3yV2adv.bin                         |
|13         | LRdifY.3yV2adv.bin                         |
|14         | LRdifZ.3yV2adv.bin                         |
|15         | LRdifIZ.3yV2adv.bin                        |
|16         | LRghat.3yV2adv.bin                         |


> and **tlist** can contain:
| **tlist** | **Time line** (default name) |
|:----------|:-----------------------------|
| 1         | Annual                       |
| 2         | JFM                          |
| 3         | JJA                          |
| 4         | Jan                          |
| 5         | Feb                          |
|...        |...                           |

  * Next, you may need to create scripts to launch the fortran routine with a SGE queuing system. Use the **create\_launch\_scripts.m** routine to do it. You need to tune the variables:
    * **patho**: This is where we print the queue files
    * **prog\_to\_compile**: This is the fortran code to compute the budget terms. If you didn't changed it from this package it is: interpBudgetallinonceS.F90
    * **prog\_to\_run**: This is compiled name of the code (by default: intBdgS\_ifort)
    * **workdir**: This is the root dir, ie where the fortran code is and where are directories of parameters and queue scripts.
    * **klist** and **tlist**: Set up them as in **create\_param\_files.m**.

  * Last but not least, you need to tune the domain size and interpolation parameters in the fortran code: **interpBudgetallinonceS.F90**. The domain size (number of grid points in each directions) is fixed in the module _mysizes_. You must have:
```
    jpi = diff(subdomain(1:2))+1;
    jpj = diff(subdomain(3:4))+1;
    jpk = diff(subdomain(5:6))+1;
```
> Interpolation parameters are **nb\_in** and **nbIn2Out**. **nb\_in** is the factor by which the program will multiply the number of grid points. Starting from the 1x1 degree Atlas, **nb\_in=12** will interpolate the field to a 1/12 degree grid. The other parameter **nbIn2Out** sets the factor by which the interpolated fields are scaled for the output fields. **nbIn2Out=3** will produce records on a 12/3=4, ie 1/4 degree grid. **_IMPORTANT_**: both **nb\_in** and the result of **nb\_in/nbIn2Out** must be even numbers (multiple of 2).

  * I almost forgot, you have to define the temperatures embedding the layer you're budgeting. Tune the parameters **THETAlow** and **THETAhig** in the fortran code.

  * You finally need to be sure your machine has the intel fortran compiler. Otherwise you'll need to tune the compilation line in the queue script files.

### Extra ###

> This is a bunch of routines to look at the results.
> If you want to do it on your own, you should know what the output files are.
For each field, you have two output files: the one with 'timeseries' in the name corresponds to the time serie of the domain integrated field, the other the 3D map of the field (time serie cumulated).
> For example in Matlab, you can try:
```
  % Your parameters here:
  iter0 = 1; 
  iter1 = 1099; 
  nt = iter1 - iter0 + 1; 
  THETAlow = 16; 
  THETAhigh = 19; 
  nb_in = 12; 
  nbIn2Out = 3; 
  nb_out = nb_in/nbIn2Out; 
  dirtofiles = '~/my_outputs_are_here/'; 

  % If you used the default set up of file names, this should be ok:
  prefi = sprintf('%s/InterpALLonce_%4.4d_%4.4d_%2.0f.m%2.0f._timeseries_',dirtofiles,iter0,iter1,THETAlow,THETAhig);
  sg = -1/3; % This is because fields are cumulated over 3 years and on the other side of the temperature tendency equation
  t = datenum(2003,11,1,0,0,0); t = t(1):t(1)+nt-1; % Time axis

  % Read outputs:

  fid = fopen(strcat(prefi,'LRvol.3yV2adv.bin'),'r','ieee-be');
  Vvol = fread(fid,[1 nt],'float32'); % Contains the layer volume time serie
  
  fid = fopen(strcat(prefi,'LRvol.3yV2adv.bin'),'r','ieee-be');
  M = fread(fid,[jpi*jpj*nb_out*nb_out jpk*nb_out],'float32');fclose(fid);
  M = reshape(M,[jpi*nb_out jpj*nb_out jpk*nb_out]); 
  Mvol = permute(M*sg,[3 2 1]); clear M
  % Mvol(x,y,z) contains the ''concentration'' of the layer

  fid = fopen(strcat(prefi,'LRairsea3D.3yV2adv.bin'),'r','ieee-be');
  Vq = fread(fid,[1 nt],'float32'); % Contains the air-sea heat flux formation rate time serie
  
  fid = fopen(strcat(prefi,'LRairsea3D.3yV2adv.bin'),'r','ieee-be');
  M = fread(fid,[jpi*jpj*nb_out*nb_out jpk*nb_out],'float32');fclose(fid);
  M = reshape(M,[jpi*nb_out jpj*nb_out jpk*nb_out]); 
  Mq = permute(M*sg,[3 2 1]); clear M
  % Mq contains the map of formation rate due to air-sea heat fluxes.

  % Note that the total integral of Mq must match the last value of Vq.
  % For all fields, the unit is Sv.y = 10^6*86400*365 ~ 3.15x10^13 m^3  
```





