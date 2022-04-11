# Postural sway analysis for Parkinson's patients
This is the online public repo for the paper: "Which features of postural sway are effective in distinguishing Parkinson’s disease patients from controls? An experimental investigation", authored by: Wenbo Ge, Deborah Apthorp, Christian Lueck, and Hanna Suominen.

This contains the code to extract features from the centre of pressure signal, used for patients with Parkinson's disease and controls. This also contains the code to determine the effectiveness of these features through several methods:
- Effect size of individual features 
- AUROC of individual features
- AUROC of all features
- AUROC of best subset of features

The AUROC was determined through a binary classifier, an ensemble model that includes logistic regression, support vector machines, and random forests.

The feature selection was done through maximum relevance (highest ANOVA F-value or highest mutal information), minimum redundancy (least Pearson's correlation), wrapper (linear-SVM with L1 penalty), dimensionality reduction (PCA).

The results can be seen in the "Experiment" notebook, which holds all results from the paper, such as images, important effect sizes, and Bayesian analysis results. For the complete results, check out the "Results" folder.

## Features:
The code extracts 102 unique features, 94 of which are repeated for eyes open and eyes closed postural sway signals, for a total of 196 features. The other 8 unique features utilised both eyes open and eyes closed signals, so are not repeated. The full list of features can be found in feature_names.csv. Alternatively, they can be found in [Table 2 of the Appendix](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1002%2Fbrb3.1929&file=brb31929-sup-0002-AppendixS2.pdf) of our previous paper: "[Which features of postural sway are effective in distinguishing Parkinson's disease from controls? A systematic review](https://onlinelibrary.wiley.com/doi/10.1002/brb3.1929)", which aimed to do the same thing, but by systematically searching the literature, rather than through experimental methods. 

## Methods:
More clarity on the methods can be found in the presentation found in the parent folder. The corresponding slides can also be found. If these are not working, a link to the presentation can be found [here](https://screencast-o-matic.com/watch/crXTndVIpGL). This was presented at IEEE BIBM 2021.

## Citation:
When using our code, please cite our corresponding paper. The citation for this and bibtex entry will be updated when the paper has been published.
