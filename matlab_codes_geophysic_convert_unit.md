## convert\_unit.m ##
Convert unit of oceanic concentration substance

[Download here](http://guillaumemaze.googlecode.com/svn/trunk/matlab/codes/geophysic/convert_unit.m)

```
% convert_unit Convert unit of oceanic concentration substance
%
% NEW_SUBST_CONTENT = convert_unit(SUBST_CONTENT,SUBST_TYPE,UNIT_IN,UNIT_OUT,[SIG0,VERBOSE])
% 
% Convert concentration of substance SUBST_CONTENT of type SUBST_TYPE 
% from UNIT_IN to UNIT_OUT.
%
% Inputs:
%	SUBST_CONTENT: a double array of any dimensions
%	SUBST_TYPE:
%		'OXY'  for Oxygen (O2)
%		'PHOS' for Phosphate (PO4)
%		'NITR' for Nitrate (NIO3)
%		'NIO2' for Nitrite (NIO2)
%		'SIO3' for Silicate (SIO3)
%		'SIO4' for Silice (SIO4)
%	UNIT_IN is a string with format: NUMERATOR/DENOMINATOR with:
%		NUMERATOR   = 'mol';'mmol';'mumol';'kg';'g';'mg';'l';'ml'
%		DENOMINATOR = 'kg';'g';'m3';'l';'ml'
%		Any combination is allowed.
%	UNIT_OUT: idem as UNIT_IN
%	SIG0 is a singleton or a double array of SUBST_CONTENT dimensions.
%		It contains the anomalous potential density referred to the sea
%		surface in kg/m3.
%		Conversion is computed with RHO = 1000 + SIG0.
%		If SIG0 not specified, it is set to 0.
%	VERBOSE (0/1) prints information about the conversion on screen (0 by default).
%
% Example:
%	convert_unit(300,'OXY','mumol/kg','ml/l',0,1)
%	convert_unit(9,'OXY','ml/l','mmol/l',32,1)
%
% Rq:
%	Molar mass (g/mol):
%		O  = 15.9994;   % Oxygen
%		P  = 30.973762; % Phophorus
%		Si = 28.0855;   % Silicon
%		N  = 14.0067;   % Nitrogen
%		(Source: http://www.iupac.org/publications/pac/2006/pdf/7811x2051.pdf)
%	Molar volume (l/mol):
%		OXY = 22.3916; % at standard temperature and pressure (Garcia and Gordon, 1992).
% 		% Note that for an ideal gas it is: 22.413
%		...
%	The molar volume for other substances is not documented right now, so any conversion from
%	mole to liter is impossible and will return NaN. Only mole <-> kg
%	Well, OXY is a gaz while other substances are ions, so it's not so surprising. Beside, most
%	current conversions are from mumol or mmol per m3 to per l and thus do not involved molar
%	volumes.
%
% Other source: http://www.helcom.fi/groups/monas/CombineManual/AnnexesB/en_GB/annex9app3/
%
% Created: 2009-09-16.
```

---

Last update: 2014 May 07, 17:43

Created by Guillaume Maze

More informations at: [codes.guillaumemaze.org/matlab](http://codes.guillaumemaze.org/matlab)