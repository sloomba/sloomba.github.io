<img vspace="10" hspace="10" align="right" width="200" height="200" src="/images/sloomba.jpg">
I am a research fellow supervised by [Prof. James J. Collins](http://collinslab.mit.edu/) at the [Wyss Institute for Biologically Inspired Engineering](https://wyss.harvard.edu/) at [Harvard University](https://www.harvard.edu/). I presently work at the intersection of computer science (mostly Bayesian nonparametrics and deep probabilistic programming) and biology (mostly systems and synthetic biology). 

I did my B.Tech in Computer Science and Engineering at [IIT Delhi](http://www.iitd.ac.in/), where my research was primarily guided by [Dr. Sumeet Agarwal](http://web.iitd.ac.in/~sumeet/research.html). My bachelors' thesis focused on building causal models of gene regulatory networks.

My broad research interest is to apply mathematics and machine learning to better understand how complex biological, cognitive and eventually social systems work.

I also write sporadically on my [Medium](https://medium.com/@sahilloomba) about things that cross my mind. 

[Curriculum Vitae](/docs/sahilloomba_cv.pdf) | [Google Scholar](https://scholar.google.com/citations?user=uuwcbrAAAAAJ) | Email: <sahil.loomba@wyss.harvard.edu>

# Research

I believe computation is a vital tool for understanding things at all levels of organization of the world. Right from the fundamental particles of the universe, to the biomolecules that make life possible, to the wonders of biological intelligence, up to the intricate social interactions that create human civilization. Although most of my work focuses on biological and cognitive systems, I like to situate my research in the context of this organizational hierarchy.

![Hierarchical Organization of the World](/images/organization_of_the_world.jpg)
*Hierarchical Organization of the World*

Notice that there is a lot of shared structure of problems at various levels of the hierarchy, for instance the prevalance of graph structures at the biological, cognitive and societal levels. This pattern, when abstracted out, is precisely what permits the use of computation at every organizational level.

# Computation Core

### X-t-SNE
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_xtsne.jpg">
[t-Stochastic Neighbor Embedding](https://lvdmaaten.github.io/tsne/) is a method of visualizing very high-dimensional data in 2 or 3 dimensions, that is now ubiquitiously used in data analysis across disciplines. The standard implementation allows visualization of a single feature space. We extend t-SNE to multiple feature spaces that could have an associated graph structure. That is, every data-point exists in multiple spaces, and all the data points are related in one or more graph structures. This extension is very useful since the generic graph structure can encode interesting domain knowledge that guides data visualization in the low-D space.

slides | code | video

### iWMMM
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_iwmmm.jpg">
[Gaussian mixture models](https://en.wikipedia.org/wiki/Mixture_model#Gaussian_mixture_model) are popular for clustering problems, where every cluster is assumed to be generated from a Gaussian distribution in the feature space. Placing a Dirichlet process prior on this space allows us to also automatically discover the number of clusters in the feature space, known as [infinite Gaussian mixture models](https://www.seas.harvard.edu/courses/cs281/papers/rasmussen-1999a.pdf). However, the assumption of a Gaussian shaped cluster could be flawed. Instead, one can assume the feature space to be the output of a mapping from a latent space, where the Gaussian assumption might hold. Assuming a Gaussian process mapping between the latent and output spaces allows us to cluster arbitrarily warped clusters, called the [infinite warped mixture model](https://arxiv.org/pdf/1206.1846.pdf). We extend this approach to when we have multiple output feature spaces, assuming each to come from an independent Gaussian process from the same latent space.

pdf | slides | code

### Hierarchical Ensemble Classifier
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_hierarchicalensemble.jpg">


# Computation for Biology

## Biomolecules

<img vspace="10" hspace="10" align="left" width="150" height="80" src="/images/thumb_protein2vec.jpg">
### protein2vec
Defining a vector space that embeds peptide sequences for solving proteomics problems

<img vspace="10" hspace="10" align="left" width="150" height="110" src="/images/thumb_conddr.jpg">
### Project ConDDR
An information-retrieval approach to the drug repurposing problem

## Biomolecular Networks

<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_crom3top.jpg">
### Project THoR
Developing a probabilistic model of tolerance to pathogens for Technologies for Host Resilience

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_sd2.jpg">
### Project SD2
An automated pipeline for Synergestic Discovery and Design of biological circuits

<img vspace="10" hspace="10" align="left" width="150" height="80" src="/images/thumb_causalgrn.jpg">
### Causal GRNs
A causal computational model for gene regulatory networks

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_evolvablenetworks.jpg">
### Evolvable Networks
A principled approach of defining biological networks that evolve

## Biological Cells

<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_apoptosis.jpg">
### Game of Apoptosis (You Live or You Die)
A simulation of a Boolean network model of programmed cell death

<img vspace="10" hspace="10" align="left" width="150" height="110" src="/images/thumb_maldi.jpg">
### Project MALDI for Diagnosis
A probabilistic model for detection of infectious pathogens

## Human Body

<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_abbie.jpg">
### Project Abbie
Analysis of breathing waveforms for preemptive prediction of an asthma attack

# Computation for Cognition

## Cellular Signalling

<img vspace="10" hspace="10" align="left" width="150" height="180" src="/images/thumb_eeg.jpg">
### Human Motor Control
A simple analysis of EEG signals for classifying motor commands issued by the brain

## Human Brain

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_prototypeexemplar.jpg">
### Human Category Learning
Studying the brain functional lateralization of two popular models of category learning

<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_formlearning.jpg">
### Human Form Learning
Extending a Bayesian model of how humans learn forms of structures of real-life entities

<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_complexitylivingbiosystems.jpg">
### Complexity of Living and Biological Systems

# Computation for Society

## Social Networks

<img vspace="10" hspace="10" align="left" width="150" height="140" src="/images/thumb_crowds.jpg">
### Wisdom of Crowds

### Pedagogy in the Contemporary World

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_mmtoc.jpg">
#### MMToC

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_videosequencing.jpg">
#### Video Lecture Sequencing

## Environment

<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_plankton.jpg">
### Plankton and Ocean Health

## Society

<img vspace="10" hspace="10" align="left" width="150" height="140" src="/images/thumb_rationalityeconomics.jpg">
### "Rationality" in Economics

<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_unsettlement.jpg">
### Unsettlment in Human Interactions
