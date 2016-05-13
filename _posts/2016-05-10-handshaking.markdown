---
layout:     post
title:         Dataset Enrichment and Handshaking
author:     Ahmet Cecen
tags: 		post
subtitle:  	Exploring ways to enrich the data.
date:       2016-05-10 02:00
---
<!-- Start Writing Below in Markdown -->

# Table of Contents

* TOC
{:toc}

# Enrichment Strategy

Since our current dataset is of limited size, we will explore benefits of adding simulated datasets of similar nature to the analysis, obtained from other sources.

# New Dataset

A potentially compatible dataset is found online published at [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/KJMK9Z
)

Microstructure results from the simulation of additive manufacturing processes with the SPPARKS Monte Carlo code. All simulations were performed on a 300 x 300 x 200 rectangular lattice. The parameters varied during the study. All length and timescales are defined within the model and refer to no actual physical system. 

![SimData](/EAB-AM-Project/img/SimData.gif)

# Length Scale Problem

Since the new data is simulated without a particular lengthscale, we need to find a way to handshake the lengthscales of the two datasets. This can be done visually like the visualization below, however we can also utilize Chord Length Distributions to come up with an objective scaling measure.

![LengthScales](/EAB-AM-Project/img/LengthScales.png)

# Using Chord Length Distributions (CLD) to Handshake Length Scales

Original difference in length scales as visible in the CLD is shown below. We fit a lognormal distribution to highlight trends.

$$ \ln\mathcal{N}(\mu,\,\sigma^2) = \frac{1}{x\sigma\sqrt{2\pi}}\ e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}} $$

![AMvsOriginalCLD](/EAB-AM-Project/img/AMvsOriginalCLD.png)

We can then scale the simulated dataset based on mean lengthscale and fit parameters with a reasonable accuracy. Here we have used a scaling factor of 3 to enlarge the simulated microsturcture. The resulting CLDs appear compatible as shown below.

![AMvsStrecthedCLD](/EAB-AM-Project/img/AMvsStrecthedCLD.png)


