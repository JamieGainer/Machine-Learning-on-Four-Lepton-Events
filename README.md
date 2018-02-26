# Machine-Learning-on-Four-Lepton-Events

## Introduction

This repository is intended to provide a toolkit and examples
for studying Higgs to four-lepton events, such as those produced
at the CERN Large Hadron Collider, using various machine learning
techniques.  Questions of interest include the sensitivity of various
approaches as well as which variables/ what physical principles drive 
that sensitivity.

Since there are two antiicpated user groups: (i) physicists interested
in machine learning and (ii) machine learning experts interested in 
physics, I will try to provide explanations that are comprehensible
to both user groups (at the risk of belaboring the obvious).

On the physics front: I am going to *initially* focus on distinguishing
the Higgs signal from the q qbar -> Z Z/gamma* backgrounds.
This is simpler from a machine learning standpoint in that we are comparing
two simple hypotheses.  Extending this to the case of measuring Higgs
properties (i.e. determining the correct point in a parameter space
describing Higgs couplings) is envisioned as a future direction.

I will now describe each subfolder of the repository, as I can
anticipate users being interested only in some of these subfolders.

## Data

This subfolder will contain the data files:
1.  100 K signal events in "MEKD" format
2.  the same 100 K signal events using angle convention from arXiv:1108.2274
3.  the same 100 K signal events using angle convention from, e.g., arXiv:1208.4018
4.  squared matrix element values for each event from MEKD
as well as corresponding event files for background events.  These files were generated using
the code found (with documentation) in the "Processing_Raw_Data" subfolder.

I should note that MEKD is a tool for calculating squared matrix elements for four-lepton events, allowing
one to use the "Matrix Element Method" to calculate the likelihood from first principles.
It is available on github (https://github.com/odysei/MEKD) and is described in
arXiv:1210.0896 and arXiv:1310.1397 of which I am a co-author.

## Logistic Regression

## Feedforward Neural Networks

## Future Directions

Future directions which are high on my to-do list:
1.  The Matrix Element Method (MEM) (see, e.g., arXiv:1108.2274, by me and collaborators)
2.  Naive Bayes (both from first principles and from the training data.  Really just to assess
how important correlations are to the MEM.)
2.  Optimized cuts from a grid search.  (Really just to have a simple baseline.)
3.  Recursive neural networks.
4.  Support vector machines.
5.  Reinforcement learning.

In general I also want to include as many different implementations of various techniques as possible
(i.e., I'd like to implement as many techniques as possible in pyTorch, tensorFlow, keras, scikit-learn,
ROOT TMVA, etc.).

## Raw Data

This folder contains small output files from MadGraph (https://launchpad.net/mg5amcnlo)
that contain the simulated signal and background events.

I emphasize *small* output files: the file formats for MadGraph
output, **LHE** (arXiv:hep-ph/0609017) and **HEPMC** (http://hepmc.web.cern.ch/hepmc/)
are not very efficient for our purposes.  So I haven't uploaded all of the events used to make
the simpler data files in the data directory, because the relevant files are too large.

These files are primarily interesting from the perspective of understanding where the data
in the "Data" subfolder comes from.

## Processing_Raw_Data

The subfolder contains notebooks and python code for
1.  Reading the four lepton momentum information into LHE and HEPMC files (such as those in the "Raw Data" subfolder)
2.  Simulating detector response
3.  Writing the output files in the "Data"

Again these files are primarily interesting either to understand where the data in the "Data" subfolder
comes from or for physicists interested in using a similar workflow to process MadGraph output files.

## References

Need to fill out...

1.  MadGraph
2.  MEKD
3.  1208.4018
4.  LHE
5.  HEPMC
6.  other...


