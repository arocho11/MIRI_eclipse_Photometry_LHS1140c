# MIRI_Eclipse_Photometry_LHS1140c
 Code to reduce and fit MIRI eclipse photometry data for LHS 1140c as detailed in "Reanalysis of the eclipses of LHS1140c: No evidence of an atmosphere and implications for the internal structure of the planet" submitted to ApJL on 13-10-2025. 

 Three eclipses were measured on Nov. 27th, July 7th and July 19th. 

 The framework is simple:

- The instrumental systematic signal is fit simulatenously with the astrophysical signal. Each eclipse can be fit separately or jointly. 

- The astrophysical signal is fit using BATMAN secondary eclipse transit model.
  
- The instrumental signal can be fit with a combination of time-dependent models as well as aa second-order polynomial centroid model, independent of time, that relies on the change in the position of the PSF. The models are exponential, linear, 2nd-degree polynomial and double exponential. The combinations that can therefore be made are: 'exp', 'exp+linear', 'exp+polynomial', 'linear+polynomial', 'polynomial', 'double_exp', 'exp_2nd_order_centroid', 'exp+polynomial_2nd_order_centroid', 'exp+linear_2nd_order_centroid', 'polynomial_2nd_order_centroid', 'linear+polynomial_2nd_order_centroid', 'double_exp_2nd_order_centroid'. 

- The joint_fit notebook can be used to constrain a single eclipse depth and time of mid-eclipse with the three eclipses jointly fitted. Each eclipse has its own coefficients for the instrumental noise model chosen, these best fit model selected by model comparison.

- The run_mcmc notebook can be used by simply importing the data and selecting the model(s) to test.

More details, supporting code and previous versions can be found at: https://github.com/arocho11/MIRI_Eclipse_Photometry_Analysis.git
