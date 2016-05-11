---
layout:     post
title:         Dataset Handshaking
author:     Ahmet Cecen
tags: 		post template
subtitle:  	Some Short Description of Post
date:       2016-05-10 02:00
---
<!-- Start Writing Below in Markdown -->

# Table of Contents

* TOC
{:toc}

# New Data, Why?

Dataset origin.

# Length Scale Problem

Describe problem.

![LengthScales](/EAB-AM-Project/img/LengthScales.png)

# Using Chord Length Distribution to Handshake Length Scales

Original difference in length scales.

Fit lognormal.

$$ \ln\mathcal{N}(\mu,\,\sigma^2) = \frac{1}{x\sigma\sqrt{2\pi}}\ e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}} $$

![AMvsOriginalCLD](/EAB-AM-Project/img/AMvsOriginalCLD.png)

Scaling based on Lognormal Fit parameters.

![AMvsStrecthedCLD](/EAB-AM-Project/img/AMvsStrecthedCLD.png)


