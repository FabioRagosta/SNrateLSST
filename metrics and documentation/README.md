The described metric aims to exploit the potentiality of LSST survey stratedy, simulated in the opsims databases. 
There are two classes of proposed metrics:
  - search of True Novelties;
  - analysis of the SN classification efficiency.
  
The metrics related to the first class are grouped in astrometry_metrics.py and they are:
  - LSmetric: the aim of this metric is to measure the fraction of detectable 'unusual object' whose proper motion is measurable;
  - TPMmetric: the aim of this metric is to measure the fraction of detectable transients whose proper motion is unusual 
  - reducedPM: the aim of this metric is to measure the accuracy of a proper motion measure in a structure to be able recognise unusual stream.
  
We propose a simulation of proper motion measures that aims to describe a known population, which is drived by a velocity distribution function such as the one in Binney 2009;
and an unusual population which is driven by a different velocity distribution function. By the use of this mock data we want to measure the fraction of the unusual population
that can be identified as a True Novelty. 

The case of unsual stream is tackled a bit differently with respect the method exposed up to now. Indeed, we use the data of Sagitarius A in Carlin et al 2012 as a toy model to measure
the possibility to detect the unusual stream they detect in the dwarf galaxy, considering to possibility:
  - having a galaxy farther away;
  - having a structure with stars in different location of the CMD.
  
The second class is composed by the metric:
  - SNclassification: the aim of this metric is to measure the fraction of detectable and correctly classifieble SNe.
  
We simulate K-corrected templates' ligh curves within a given redshift range, and we simulate an uniform explosion time distribution during the survey. 
We estimate the detected points on the light curve according to the observational contraints of the survey strategy, and imposing some threshold to difine a light curve as "detected" or "filtered_class", 
the latter meaning that the light curve pass the threshold to be injected into the classificator. 
Finally we inject the simulated observed light curve in PSNID (Sako et al.2011), which is a classification tools available in SNANA.

<img src="flowchart_SNRMetric.png">

