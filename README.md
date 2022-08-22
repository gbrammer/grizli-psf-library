# grizli-psf-library
PSF models for use with Grizli mosaics

Documentation TBD as always, but the general procedure is as follows:

1) Generate WebbPSF models in the detector frame for a given observation epoch
   with the `load_wss_opd_by_date` method recently added to WebbPSF.  The WebbPSF
   models are evaluated for 4 pixel phases in a 3x3 grid across the detector.
   
2) Insert these "effective" PSFs into dummy exposures and drizzle them with the 
   same drizzle parameters as those used to create the mosaic.
   
3) For now, the PSFs are all evaluated on the fine 40 mas pixel scale.
