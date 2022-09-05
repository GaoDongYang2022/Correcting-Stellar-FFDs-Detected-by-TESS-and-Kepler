Correcting Stellar Flare Frequency Distributions Detected by TESS and Kepler
================================================================================
Description:
Complete tables in machine-readable form for this paper. 

File Summary:
ReadMe： This file
table1.csv: Stellar parameters of each sample. Sample-1: Kepler Flaring star (Yang & Liu 2019) with TESS light-curve (13 stars, including 6 stars for rigorous analysis, see Section 4.1); Sample-2: Solar-type TESS flaring stars from Tu et al. (2020) (84 stars); Sample-3: Different type TESS flaring stars from Gu ̈nther et al. (2020) and Yang & Liu (2019) (24 stars). 
table2.csv: The power-law parameters for fitting cumulative FFDs before and after correction for flaring stars in Sample-1 were obtained through TESS and Kepler missions. 
table3.csv:  The power-law parameters for fitting cumulative FFDs before and after correction for solar-type stars (Sample-2) and different type stars (Sample-3). 

Descriptions of tables are as follows in the form “Label	Units Explanations”:

Description of table1.csv 
--------------------------------------------------------------------------------
Label 	Units        Explanations
--------------------------------------------------------------------------------
Samples ---	Sample number
TICID	 --- 	TESSInput Catalog ID
KICID	---	Kepler Input Catalog ID
Tmag 	mag	TESS magnitude
Kmag	mag	Kepler magnitude
Teff 	K	Effective temperature
Rs	Rsun	Stellar Radius
GAIAID	 --- 	GAIA Catalog ID
RUWE	--- 	Renormalised Unit Weight Error from GAIA Catalog 
Gmag	mag	G-band mean magnitude 
Teff_G	K	Effective temperature from GSP-Phot 
logg_G	log(cm.s**-2)	Surface gravity from GSP-Phot
[Fe/H]_G	dex	Iron abundance from GSP-Phot 
Rs_G	solRad	Radius from GSP-Phot
Prot	day	Rotation period
Nf_previous	count	The number of flares in previous work
Nf_TESS	count	The number of flares detected from TESS data in this work
TESS_Sector ---	TESS data used in this work
Nf_Kepler	count	The number of flares detected from Kepler data in this work
Kepler_Quarter --- Kepler data used in this work
Separation ---	The distance of the nearby star to the star
--------------------------------------------------------------------------------
Note on table1.csv:
(1)For stars in Sample-1 and Sample-2, the stellar parameters are read through astroquery.mast.Catalogs (https: //astroquery.readthedocs.io) from TESS input catalog (TIC v8) (Paegert et al. 2022); For Kelper flaring stars in Sample-3, their stellar parameters are from Berger et al. (2020); We cross match each star with GAIA Dr 3 and show the stellar parameters from the GAIA catalog.
(2) Stellar rotation periods are taken from Yang & Liu (2019), partly Given by Reinhold et al. (2013) and McQuillan et al. (2014).
(3) For Kepler flaring stars, “Nfprevious” is taken from Yang & Liu (2019); For TESS flaring stars, “Nfprevious” is taken from Gu ̈nther et al. (2020) and Tu et al. (2020).
(4) TIC 164670606 (KIC 8935655) is also listed in Sample-3. 


Description of table2.csv:
TICID, KICID, Tmag, Prot, Teff, TESS_Sector, Nf_TESS and Nf_Kepler are the same as in table1.csv
--------------------------------------------------------------------------------
Label 	Units        Explanations
--------------------------------------------------------------------------------
TIC_low_all 	--- 	The energy lower limit for cumulative FFD fitting from TESS.
TIC_upper_all	---	The energy upper limit for cumulative FFD fitting from TESS.
alp_TICOrig 	--- 	The cumulative alpha fitted within all energy range of original flares from TESS
alp_TICOrig_err ---	The error of cumulative alpha fitted within the whole energy range of original flares from TESS
beta_TICOrig 	--- 	The cumulative beta fitted within all energy range of original flares from TESS
beta_TICOrig_err ---	The error of cumulative beta fitted within all energy range of original flares from TESS
alp_TICCorr 	--- 	The cumulative alpha fitted within the whole energy range of corrected flares from TESS
alp_TICCorr_err ---	The error of cumulative alpha fitted within the whole energy range of corrected flares from TESS
beta_TICCorr 	--- 	The cumulative beta fitted within the whole energy range of corrected flares from TESS
beta_TICCorr_err ---	The error of cumulative beta fitted within the whole energy range of corrected flares from TESS

KIC_low_all 	logarithm	The energy lower limit for cumulative FFD fitting from Kepler.
KIC_upper_all 	logarithm	The energy upper limit for cumulative FFD fitting from Kepler.
alp_KICOrig 	--- 	The cumulative alpha fitted within the energy range of detection probability P_det>= 65% before flare correction from Kepler
alp_KICOrig_err ---	The error of cumulative alpha fitted within the energy range of detection probability P_det>= 65% before flare correction from Kepler beta_KICOrig --- 	The cumulative beta fitted within the energy range of detection probability P_det>= 65% before flare correction from Kepler
beta_KICOrig_err --- 	The error of cumulative beta fitted within the energy range of detection probability P_det>= 65% before flare correction from Kepler
EngLow_Range65 	logarithm	The energy lower limit for cumulative FFD fitting within the energy range of detection probability P_det>= 65% from Kepler

alp_KICCorr	 --- 	The error of cumnlative alpha fitted within the energy range of detection probability P_det>= 15% after flare correction from Kepler 
alp_KICOCorr_err ---	The error of cumnlative alpha fitted within the energy range of detection probability P_det>= 15% before flare correction from Kepler
beta_KICCorr --- 	The error of cumnlative beta fitted within the energy range of detection probability P_det>= 15% after flare correction from Kepler 
beta_KICOCorr_err ---	The error of cumnlative beta fitted within the energy range of detection probability P_det>= 15% before flare correction from Kepler
EngLow_Range15 	logarithm 	The energy lower limit for cumulative FFD fitting within energy range of detection probability P_det>= 15% from Kepler
--------------------------------------------------------------------------------
Note on table2.csv:
(1) When fitting the cumulative FFDs, we use the flare energy of each event calculated from the stellar parameters from GAIA catalog.
(2) Because of the requirement of sufficient energy bins, we use the whole energy range to fit the cumulate FFDs obtained from the TESS data for Sample-1 stars. 


Description of table3.csv 
Samples, TICID, and KICID, are the same as in table1.csv.
--------------------------------------------------------------------------------
Label 	Units        Explanations
--------------------------------------------------------------------------------
*_alp_orig 	---	The cumulative alpha fitted before flare correction from TESS or Kepler
 *_alp_origerr	--- 	The error of cumulative alpha fitted before flare correction from TESS or Kepler
*_beta_orig 	--- 	The cumulative beta fitted before flare correction from TESS or Kepler
*_beta_origerr	--- 	The error of cumulative beta fitted before flare correction from TESS or Kepler

*_alp_corr 	---	The cumulative alpha fitted after flare correction from TESS or Kepler
 *_alp_correrr	--- 	The error of cumulative alpha fitted after flare correction from TESS or Kepler
*_beta_corr 	--- 	The cumulative beta fitted after flare correction from TESS or Kepler
*_beta_correrr	--- 	The error of cumulative beta fitted after flare correction from TESS or Kepler

all_* 	--- 	The cumulative FFD fitting within the whole energy range. 
Up15_* 	--- 	The cumulative FFD fitting within energy range of detection probability P_det>= 15%. 
Up65_* 	--- 	The cumulative FFD fitting within energy range of detection probability P_det>= 65%. 
--------------------------------------------------------------------------------
Note on table3.csv:
(1) When fitting the cumulative FFDs, we use the flare energy of each event calculated from the stellar parameters from GAIA catalog.
(2)	The alpha of cumulative FFD in previous work can be obtained from Gu ̈nther et al. (2020)

