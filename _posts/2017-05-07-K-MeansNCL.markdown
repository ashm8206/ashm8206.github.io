---
layout: post
title:  "Clustering DNA sequences"
date:   2017-05-17 08:43:59
author: Aishwarya Mali
categories: datascience

---

After graduating from Pune Institute of Computer Technology with a placement at a reputed software firm,I decided to pursue my inclination towards datascience.I completed an online course on Data-science from Dataquest.io, and then took the
internship at NCL where I worked as a project intern at National Chemical
Laboratory (NCL) with Dr. Leelavati Narlikar.

This blog post is a snapshot of all the duties I carried out there.

I performed Modified-Kmeans clustering, given sample of AGCT sequences generated from dirichlet distribution.
The algorithm was as follows,
* Arbitarily partition data into k clusters, calculate Фk for all k where 
   Фk = log(<sub>i=1</sub>∏<sup>n</sup> P(Xi |Zi=1)))
* Repeat
  * (re)assign each object to the cluster to which it is most similar based on Фk  calculate w.r.t to each k . Assign to   cluster n if the value the maximizes on Фn
* Recompute Ф for all k
  Until no change

I inititally designed an the above algorithm in pandas, a grave mistake. I varied the values of the length of the sequences and number of sequences and plotted a number of graphs w.r.t time as the performance matrix.The result was not promising. The newly designed algorithm took the same time as the current system in place.I found out not quite suprisingly that time taken to convergence was directly ∝  to length of sequences and number of clusters. This is pretty much obvious,since there was a loop to measure probability at each position in each sequence and another loop to check likelihood for each cluster.

I think we are slowly beginining to understand why Pandas was such a bad idea. But just to be clear here are some reasons why,
1. Repeated apply function calls make pandas heavy in computation time
2. Indexing operation of pandas,aligns series on their indexes on every function call
3. Numpy array are contiguous blocks of memory so there is almost no indexing
4. Vectorization in numpy,applies an operation to all elements in an array

