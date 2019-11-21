---
layout: page
title: "About the Model"
sitemap: false
permalink: "/about-the-model/"
breadcrumb: true
header:
    image_fullwidth: "canyonland_bis.jpg"
    title: ""
---



## Origins

DREAM is based on the spectral primitive equation model code first introduced by Hoskins and Simmons (1975). This code was initially used to study baroclinic wave lifecycles and quickly became one of the staple tools for dynamical studies at the Reading University Meteorology department, pressed into service for a diverse range of topics in synoptic meteorology and global climate dynamics. As a purely dynamical model, it lacks the physical source terms that maintain the climate, so for longer integrations, or for studies of perturbations on a specified basic state, a prescription is needed for the right hand side of the equations. Various solutions have been implemented, and as the model was used for more sophisticated applications, further representations of physical processes were added. At the same time a sequence of technical modifications were also made to simplify the code and make it more portable. 

The model is now known as the “igcm” and the current version (Joshi et al, 2015) is shared by a consortium of users at UK universities (see [website here](http://www.met.reading.ac.uk/~mike/dyn_models/igcm/)).


## Empirical Forcing

The problem of how to force a simple dynamical model to produce an equilibrium climate solution has often been approached by using relaxation forcing. An idealised radiative convective equilibrium temperature field is specified, and the atmospheric state is relaxed linearly towards this equilibrium on a chosen timescale. Since this radiative convective equilibrium state is hydrodynamically unstable, the atmosphere never attains this state, nor even approaches it closely (unless a very short relaxation timescale is imposed). So it is difficult to appeal to data to deduce directly what this state should be. 

The DREAM model is based on an alternative approach first used by Roads (1987) to make a cheap forecast model. A sequence of observed initial conditions is used and an unforced model is integrated for just one timestep. The negative average of the one-timestep tendencies thus produced is then adopted as the forcing on the right hand side of the model equations. If it is assumed that the set of initial conditions represents a stationary climate state, and that the forcing of the atmosphere can be viewed as time independent, this forcing term represents the missing forcing that corrects the systematic errors of an unforced model.

Some form of dissipation is also included, and the combination of forcing and dissipation is mathematically equivalent to the relaxation forcing approach discussed above. But instead of specifying an unknown equilibrium state and a damping timescale, we specify the damping timescale and appeal to data to furnish the forcing. 

The result is a GCM that is simple in conception, based entirely on dynamics, but giving realistic enough simulations to be used for a variety of climate studies. 

DREAM can also be used in perturbation mode. The only thing that changes is that the forcing is designed to hold a fixed basic state in place, as first employed by Jin and Hoskins (1995). A perturbation is then added either to the forcing, as done by Jin and Hoskins, or to the initial condition (see for example Hall and Sardeshmukh, 1998) and the model solution arising from the perturbation can be analysed. If the perturbation is constrained to be small, the solution will be linear. 


## DREAM features

In its simplest form DREAM is a dynamical model that either simulates a perpetual season or can be used to study perturbations about a fixed basic state, in both cases with time-independent forcing. 
An extension to the forcing has recently been developed that includes an annual cycle. In this way DREAM can be used for climate studies in which a one-to-one correspondence with historical data is required. 

DREAM is designed to work with the reanalysis data that is used to calculate the empirical forcing. This dataset can be consulted during a run to constrain predefined regions of the world to a time sequence of observations by “nudging” on a specified timescale. 

Further extensions to DREAM are under development, including interaction with moist thermodynamics associated with the model’s specific humidity variable. 

Further details of the DREAM model can be seen in  [this training course presentation](http://www.legos.obs-mip.fr/members/hall/dream_training_handout?lang=fr).

DREAM has been used for a wide range of applications, including fundamental properties of the midlatitude jets, teleconnections from tropical convection, the annual cycle and easterly waves over West Africa. A complete list of publications is given [here](https://dream-gcm.github.io/publications/). 
