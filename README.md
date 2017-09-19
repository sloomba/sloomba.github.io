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

slides | video | code

### iWMMM
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_iwmmm.jpg">
[Gaussian mixture models](https://en.wikipedia.org/wiki/Mixture_model#Gaussian_mixture_model) are popular for clustering problems, where every cluster is assumed to be generated from a Gaussian distribution in the feature space. Placing a Dirichlet process prior on this space allows us to also automatically discover the number of clusters in the feature space, known as [infinite Gaussian mixture models](https://www.seas.harvard.edu/courses/cs281/papers/rasmussen-1999a.pdf). However, the assumption of a Gaussian shaped cluster could be flawed. Instead, one can assume the feature space to be the output of a mapping from a latent space, where the Gaussian assumption might hold. Assuming a Gaussian process mapping between the latent and output spaces allows us to cluster arbitrarily warped clusters, called the [infinite warped mixture model](https://arxiv.org/pdf/1206.1846.pdf). We extend this approach to when we have multiple output feature spaces, assuming each to come from an independent Gaussian process from the same latent space.

pdf | slides | code

### Hierarchical Ensemble Classifier
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_hierarchicalensemble.jpg">
Many multi-classification problems have [multiple output labels](https://en.wikipedia.org/wiki/Multi-label_classification), wherein the same feature space has more than one output labels. The classification problem might be "easier" for some labels over others. With that intuition in mind, we develop a hierarchical metaclassifier which conditions single-label classifiers at lower levels on the class predicted for labels at the upper levels. That is, more difficult classification problems are conditioned over the easier ones. This flexible model can use any off-the-shelf multi-class single-label classifier at each of the levels. We test our algorithm on a two-label multi(2x4)-class problem of predicting the tolerance and pathogen of infection of a cohort of patients.

pdf | slides | code

# Computation for Biology

## Biomolecules

### protein2vec
<img vspace="10" hspace="10" align="left" width="150" height="80" src="/images/thumb_protein2vec.jpg">
Defining a vector space that embeds peptide sequences for solving proteomics problems

### Project ConDDR
<img vspace="10" hspace="10" align="left" width="150" height="110" src="/images/thumb_conddr.jpg">
An information-retrieval approach to the drug repurposing problem

## Biomolecular Networks

### Project THoR
<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_crom3top.jpg">
Developing a probabilistic model of tolerance to pathogens for Technologies for Host Resilience

### Project SD2
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_sd2.jpg">
An automated pipeline for Synergestic Discovery and Design of biological circuits

### Causal Computational Models for GRNs
<img vspace="10" hspace="10" align="left" width="150" height="80" src="/images/thumb_causalgrn.jpg">
Gene Regulatory Networks (GRNs) hold the key to understanding and solving many problems in biological sciences, with critical applications in medicine and therapeutics. However, discovering GRNs in the laboratory is a cumbersome and tricky affair,
since the number of genes and interactions, say in a mammalian cell, are very large. We aim to discover these GRNs computationally, by using gene expression levels as a time-series dataset. We research and employ techniques from probability and information theory, theory of dynamical systems, and graph structure estimation, to establish pairwise causal relations between genes on synthetic datasets. Furthermore, we suggest methods for global estimation of gene networks by using a random-walk based weight propagation algorithm.

pdf | slides | code

### Evolvable Networks
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_evolvablenetworks.jpg">
Biological networks, may they be gene regulatory networks or protein-protein interaction networks, tend to possess certain attributes. They are highly modular, seem to be very robust, and also seem to be scale-free. Thus, one might be tempted to believe that to create instances of biological networks, one must explicate such conditions on a graph. However, we hypothesize that these are merely emergent properties which are not evidently very principled. Rather, a certain sense of "evolvability" (E), combined with "robustness" (R), and some sense of "cost of complexity" (C) levied on the network, seem to be more principled evolutionary factors due to which biological networks might organize themselves. Armed with this intuition, we evolve biological networks by incorporating ERC into a genetic algorithm's objective function. The networks so obtained appear to observe the properties of modularity, scale-freeness and robustness.

slides |

## Biological Cells

### Project MALDI for Diagnosis
<img vspace="10" hspace="10" align="left" width="150" height="110" src="/images/thumb_maldi.jpg">
The purpose of this project is to identify *Mycobacterium tuberculosis* within biological fluids, particularly human urine, for use as a diagnostic. We currently have extracted pathogen from solution using FcMBL magnetic nanobead technology. The captured material is then analyzed using matrix-assisted laser deionization time-of-flight/time-of-flight [(MALDI-TOF/TOF)](https://en.wikipedia.org/wiki/Matrix-assisted_laser_desorption/ionization) tandem mass spectrometry. This produces a series of peaks specifying the mass-to-charge ratios of the sample of interest. Peak libraries exclusive to several strains of *M. tuberculosis* as well as other microbes including *Staphylococcus aureus* and *Candida albicans* have been assembled. We created a probabilistic model from these libraries in order to identify a pathogen from an unknown sample.

pdf | [webapp](https://sloomba.shinyapps.io/maldi/)

### Game of Apoptosis (You Live or You Die)
<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_apoptosis.jpg">
[Apoptosis](https://en.wikipedia.org/wiki/Apoptosis) refers to one of the many biochemical process that take place inside a cell. Known as "programmed cell death", it leads to fatal changes in the cell such as decay and DNA fragmentation. It is a highly controlled and regulated process, whose understanding can throw light on critical diseases such as cancer (under-regulated apoptosis leads to cell proliferation) and atrophy (over-regulated apoptosis leads to excessive cell death). There are multiple ways to understand regulatory networks, such as using ordinary differential equations, or using graphical methods like Bayesian and Boolean networks. The latter capture basic activating/inhibitory relationship between genes being in an on-off state (0/1, thus Boolean). We analyze one such Boolean model given by [Mai et al. (2009)](https://www.ncbi.nlm.nih.gov/pubmed/19422837), devise metrics of studying the irreversibility of apoptosis, and improve the analysis of which initial cell states are more likely to lead to apoptosis.

slides | code

## Human Body

### Project Abbie
<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_abbie.jpg">
Asthma is a common inflammatory disease of lung airways which affects millions of people across the world. An asthmatic fit can be triggered by allergens and is accompanied by symptoms such as wheezing, shortness of breath and chest spasms. A timely prediction of the fit can allow an asthmatic to seek help and administer a response on time, which could be life saving. As part of [Project Abbie](https://wyss.harvard.edu/technology/project-abbie/), in collaboration with [Boston Children's Hospital](http://www.childrenshospital.org/), we collected breathing waveform data of children from the beginning to end of an asthmatic fit, and the corresponding severity score through this timecourse. We extracted a [multifractal spectrum representation](https://en.wikipedia.org/wiki/Multifractal_system) of the signal; hypothesized and validated that the onset of an attack is accompanied by a change from mono to multifracticality of the breathing waveform. We built a simple 2-class model to predict a high/low severity score of an asthmatic over a 10-second time window, which can allow real time monitoring of patients.

pdf | slides 

# Computation for Cognition

## Cellular Signalling

### Human Motor Control
<img vspace="10" hspace="10" align="left" width="150" height="180" src="/images/thumb_eeg.jpg">
Recent advances in modern brain-imaging techniques have hugely bolstered research in areas of brain sciences and cognitive studies. While they were earlier being used for merely diagnosing brain disorders, they are now being used to generate highly utilitarian bits of data. One such imaging technique is electroencephalography, or EEG, which essentially measures the averaged electrical potential across the human scalp. The motivation behind this project was to develop a computational basis for developing real-time brain controlled actions, such as thought-controlled prosthetic limbs or electronic devices. Can we recover signatures of motor activity, or the thought of motor activity, from the EEG signal? We conduct controlled experiments to collect EEG data. Using techniques from machine learning, we then classify them into three motion states of rest, arm jerk, and thought of arm jerk.

pdf | slides

## Human Brain

### Human Category Learning
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_prototypeexemplar.jpg">
Human cognitive systems rely heavily on how knowledge is represented within these systems. One kind of knowledge, namely the categorical, is ubiquitous in everyday human interaction with the world. Two competing theories of how humans learn and infer from
category knowledge have been popular in cognitive psychology: the exemplar theory and the prototype theory. Also, like most cognitive functions, category representations have purported to be lateralized in the brain: with the left hemisphere operating under prototype
conditions, and the right hemisphere operating under exemplar conditions. We explore the hypothesis as to whether category knowledge representation is indeed lateralized in the light of these theories, and if yes, then whether a transfer of control between
the two gets activated at some epoch of learning. We conduct divided visual field tasks to collect data, and use Bayesian model selection to test our hypothesis.

pdf | slides | code

### Human Form Learning
<img vspace="10" hspace="10" align="left" width="150" height="220" src="/images/thumb_formlearning.jpg">
Given the resource constraints that human cognitive systems operate under, how do adults and children inductively learn from the percepts we encounter? Certainly, there are some heuristics involved in not just our inductive learning, but also in the way we do inference and reasoning. Can we explain away the use of such “shortcuts” by improving current computational cognitive models? This project was an attempt in answering such questions, by taking the work by [Kemp et al. (2008)](http://www.pnas.org/content/105/31/10687.full) on form learning as a neat illustration of some key ideas. We extend their work by stressing on the need to include topology theory (manifold learning) and hierarchical Bayesian modelling, by providing experimental results to support our stance.

pdf | slides

### Complexity of Living and Biological Systems
<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_complexitylivingbiosystems.jpg">
The central objective of recent strides taken by biology and biochemistry has been to simplify the complexity of biological systems, and of life itself. The theories and models we propose, and the questions we try to answer, are subject to the current limits of our mathematics and computational abilities. There are, of course, various problems in computer science that have been deemed unsolvable (like the Halting Problem), or computationally intensive (like the Maximum Independent Set Problem which is NP hard), but can similar limits be imposed on problems in biology? Our intuition tells us yes, and recent advances in the theory of computation, and the principles of Computational Equivalence and Computational Irreducibility are in overwhelming support of this intuition. We follow these principles and view systems under the lens of computational pragmatism, to uncover the possible limits imposed on our understanding of life, the way we know it.

pdf |

# Computation for Society

## Social Networks

### Wisdom of Crowds
<img vspace="10" hspace="10" align="left" width="150" height="140" src="/images/thumb_crowds.jpg">
Wisdom of Crowds refers to the idea that the aggregated opinion of a crowd of non-experts could be as close or even better than the estimate of an expert. People from across disciplines, cognitive scientists, social scientists, computer scientists and mathematicians, are trying hard to test the validity of this conjecture. In the hopes of elucidating conditions under which it holds well, areas where this can be applied, and the relation of an individual's cognitive abilities to the judgement of the crowd. As part of a large international team of students, we developed a large-scale online game to systematically investigate the wisdom of crowds. 

[paper](http://dl.acm.org/citation.cfm?id=2815725) | [webapp](https://wisdomofcrowds.stanford.edu/web/index.php#/)

### Pedagogy in the Contemporary World

#### MMToC
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_mmtoc.jpg">

#### Video Lecture Sequencing
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_videosequencing.jpg">

## Environment

### Plankton and Ocean Health
<img vspace="10" hspace="10" align="left" width="150" height="130" src="/images/thumb_plankton.jpg">
Born out of a Kaggle competition, classifying ocean plankton is an important step to be able to quantify the health of oceans. This is essentially a large multi-class problem, with close to 120 classes of plankton to be classified, with highly skewed low-resolution image data. We apply a library of image processing techniques which can characterise the shape of one plankton from another: shape descriptors (circularity constant, Hu moments), orientation descriptors (Gabor filtered data, HoG vectors), feature descriptors (SIFT), and information descriptors (Fourier analysis). We follow this by a library of machine learning techniques, from support vector machines, to random forests, to neural networks. Taking inspiration from the biological domain, we created hierarchically stacked classifiers mimicking the phylogeny tree structure of plankton classes. This increased accuracies on test data, from as low as 14% on a standard SVM, to as high as 82% on stacked SVMs.

slides | code

## Society

### Rationality in Economics
<img vspace="10" hspace="10" align="left" width="150" height="140" src="/images/thumb_rationalityeconomics.jpg">
The most foundational assumption in all of microeconomic theory is that of rationality: *Homo economicus* is an agent who is actuated only by self-interest. But there has been a lot of criticism for this key assumption, with counterexamples in the form of [tragedy of the commons](https://en.wikipedia.org/wiki/Tragedy_of_the_commons), and Sen's [Liberal Paradox](https://en.wikipedia.org/wiki/Liberal_paradox). We explore the "rationality" of this human economic agent, motivated by Daniel Hausman's anthology of essays ["Philosophy of Economics"](https://books.google.com/books/about/The_Philosophy_of_Economics.html?id=1S5GraRCFsgC) wherein he urges economists to not trust in the success of economic theories just because they seem to work, but to "look under the hood". We look at arguments by Hirschman (against parsimony), Gneezy & Rustichini (against ceteris paribus) and Benabou & Tirole (for inclusion of social norms). Sen's seminal paper, [Rational Fools](http://omega.cc.umb.edu/~pubpol/documents/Rationalfools--Sen.pdf) captures a similar sentiment into the idea of meta-preferences over usual preferences, ranked by laws and norms of the society. We propose an alternative look at economic theory, wherein theory is not founded on irrational assumptions of rationality. Rather, it is a constantly updated set of theories, driven by a previous iteration of policy making and public reaction.

pdf | slides

### Morality of Unsettling Interventions
<img vspace="10" hspace="10" align="left" width="150" height="100" src="/images/thumb_unsettlement.jpg">
Unsettlement of our personal fundamental beliefs is a common occurrence in human interactions that allows people to update their beliefs about the world. This interventionary process can eventually define collective choice of a people. But it also places an interesting moral dilemma on the participants of the intervention: "is it *right* to unsettle someone else's core beliefs?" and "should I *let* myself get unsettled?" We present an abstraction of the cognitive machinery of the agents involved in this moral problem, the way they represent knowledge and beliefs, and offer a way to resolve this dilemma for both the unsettler and the one unsettled.

pdf | slides
