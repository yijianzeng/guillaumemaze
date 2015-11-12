## convert\_oxygen.m ##
O2 unit conversion

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/convert_oxygen.m)

```
% convert_oxygen O2 unit conversion
%
% [valout] = convert_oxygen(valin,uin,uout,[aST0])
% 
% !!! Now call convert_unit routine to convert oxygen !!!
%
% Cette fonction convertit les donnes d'oxygne d'une unit  l'autre.
% Voir: convert_unit
%
% valout   = valeur d'oxygene converties dans l'unit uout 
% valin    = valeur d'oxygene en entre dans l'unit uin 
% aST0     = anomalie de densit potentielle rfrence  0 de l'eau 
%			considre, si aucun valeur n'est entre, on considre qu'on 
%			a de l'eau douce et l'anomalie de densit est nulle 
%			(rho=1000) sinon rho = 1000 + aST0 
%
% uin et uout sont: 
% 	ml/l: milli litre par litre 
% 	mmol/m3: milli mole par mtre cube 
% 	mumol/l: micromole par litre 
% 	mg/l : milli gramme par litre 
% 	mumol/kg : micromole par kilo 
% 	ml/l * 44.66 = mmol/m3 = mumol/l 
% 	ml/l*1.42903 = mg/l 
% 	mg/l * 44.66/1.42903 = mumol/l =mmol/m3 
% 	mumol/l = (rho/1000)* mumol/kg
%
%
% Created: 2008-05 by C.LAGADEC
% Rev. by Guillaume Maze on 2009-11-05: Now call convert_unit routine to convert oxygen !
% Rev. by Guillaume Maze on 2009-07-31: Moved unit to lower string for flexibility
% Rev. by Guillaume Maze on 2009-09-02: Add micromol to millimol automatic conversion
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)