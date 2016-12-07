---
layout: post
title: All About That Bayes
---

This project required us to build a model that would define distribution parameters and linear regression line for a set of data points related to tidal height at given times. The data set had 100 data points and we assumed the points were normally distributed. Here are a look at the tidal heights across time:

![Tide Data](/images/Posts/TideData.jpg)

The plot suggests a sine curve to the data, so a mu function was chosen on the order of A(sin(B(x-c))) + D, which after a lot of hand-wringing, was linerized to the form A + Bsin(x) + Ccos(x). This was plugged into our likelihood log function multiplied by our prior, which was then fed into the emcee sampler with 40 walkers each going 100,000 steps (4 million total samples). We were then given values for our three parameters and lambda (rounded here): A = 9.477, B = -0.605, C = 1.804, Lambda = 0.097, and a regression line fitting our data:

![Tide Data](/images/Posts/TideDataReg.jpg)

The fit looks good especially given our small inital data set and number of visual outliers. 

The next step for this model will be to remove some of its rigidity; right now it is hard-coded to onyl accept log funtions with three parameters and a lambda, and said log function is created outside the Class created. Assuming a normal distribution, the user should only need to submit the mu fuction, prior, and number of desired walkers, and let the model take care of the rest. Until next time...

Acknowledgements:

A good deal of the original code for this project was adapted from class lectures and jupyter notebooks created by Kilian Scheltat. I also worked closely with Alex Motamed, John Snyder, Ellen Kim, Guillermo Kopp, and James Larkin.
