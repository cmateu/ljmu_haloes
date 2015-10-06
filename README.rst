LJMU Halo Mock Catalogues
==========

The LJMU*_KIII folders contain mock catalogues for K giant stars in different Haloes from Andreea Font's LJMU Gas-Dynamical simulations (Font et al. in prep). We have used Ben Lowing's code (2015) to resample star particles into individual stars, and Xue et al. (2014) criteria to select K giant stars.

Two types of files are available in each of the LJMU*_KIII folders: the \*.ne and the \*.pe files. The \*.ne files include *all* stars in the simulation and all quantities in the catalogue are error-free. The \*.pe files are the Gaia mock catalogues and include only stars observable by Gaia (G<20), both error-free and error-convolved quantities are reported here.The error prescriptions used are described below.

In all cases, stars in given file come from a single progenitor whose corresponding ID is indicated in the file name (LJMU001_KIII.id???.ne.hel.dat.bz2).

Error prescriptions
-------------------

Proper motion and radial velocity errors have been simulated with Gaia error prescriptions as of Jun-2015 in Merce Romero’s Gaia error code. Photometric distance errors of 20% have been simulated for K giant stars (these precisions are achievable using Gaia data for photometric distance measurements). The simulation of observables includes the effect of extinction, based on the 3D reddennig map from Drimmel et al. (2003). The Sun has been placed at X=8 kpc with a velocity of (0,220,0)km/s. 


Catalogue file structure:
-------------------------

The error-free (\*.ne) files have the following structure:

- Av, XV, Gmag, Grvs : V-band extinction, V-band, G and Grvs apparent magnitudes. 
- relerr: relative parallax error 
- X, Y, Z, VX, VY, VZ : error-free cartesian galactocentric coordinates (kpc) and velocities (km/s)
- par_mas, l_deg, b_deg, Rhel_kpc, mulst_mas, mub_mas, vrad : error-free heliocentric spherical coords (parallax in mas,l and b in deg, heliocentric distance in kpc, proper motions in mas/yr, radial velocities in km/s)

*Note*: in these files Gmag,Grvs,relerr are set to dummy values of 0.000.
(note: mulst denotes the reduced proper motion in longitude, i.e. mulst=mul*cosb)

The error-convolved (\*.pe) files have the following structure:

- Av, V, Gmag, Grvs : V-band extinction, V-band, G and Grvs apparent magnitudes
- relerr: relative parallax error 
- xX ,xY ,xZ ,xVX ,xVY, xVZ : error-free cartesian galactocentric coordinates (kpc) and velocities (km/s)
- xpar_mas, xl_deg, xb_deg, xRhel_kpc, xmulcosb_masyr, xmub_masyr, xvrad : error-free heliocentric spherical coordinates (parallax in mas, l and b in deg, heliocentric distance in kpc, proper motions in mas/yr, radial velocities in km/s)
- gX, gY, gZ, gVX, gVY, gVZ : error-convolved cartesian galactocentric coordinates and velocities.
- gpar_mas, gl_deg, gb_deg, gRhel_kpc, gmulcosb_masyr, gmub_masyr, xvrad : error-convolved heliocentric spherical coordinates
- relerr_D, sig_mub, sig_vrad, VI, relerr_mub, relerr_vrad : relative distance error, proper motion error in mas/yr (std. dev.), radial velocity error in km/s (std. dev.), apparent V-I colour, relative proper motion error, relative radial velocity error

*Note*: This data is the same as in the `Gas-Dynamical challenge in the III Gaia Challenge Wiki <http://astrowiki.ph.surrey.ac.uk/dokuwiki/doku.php?id=tests:streams:challenges#gas-dynamical_challenge>`__ (\*.gerr.dat files), only the data here has been split into individual files according to the progenitor ID (IDstream). 

For any questions please contact: Cecilia Mateu (cmateu at cida.gob.ve) or Andreea Font (A.S.Font at ljmu.ac.uk) 

