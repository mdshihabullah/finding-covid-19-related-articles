# Finding Covid-19 related articles from scientific journal using Naive Bayes classifier

In this project, I have tried to find out whether the articles available in one of the
recommended dataset comprising scientific publications are COVID-19 related or not
using Naive Bayes classifier.

Various utility steps, function and core methods undertaken to achieve the tasks are
mentioned and coded both with comments and required documentation in the submitted Jupyter notebook file.

# Project Description:

## Getting the data:
You will need to download scientific article data from https://ftp.ncbi.nlm.nih.gov/pub/pmc/oa_bulk/
With the documentation here: https://www.ncbi.nlm.nih.gov/pmc/tools/openftlist/
As the files are quite large you can constrain your study to files comm_use.I-N.xml.tar.gz
and non_comm_use.I-N.xml.tar.gz, although you are free to analyze the contents of all the files if you so 
wish.
You should use the [PMCID].nxml files.

## Analysis
Using the titles and abstracts extracted from .nxml files create a suitable normalization pipeline. Describe 
what normalization steps you are using and what these are achieving in terms of structuring raw text.
Create a classifier that based on publication title and abstract, makes a determination whether the paper is 
about COVID-19 or not. You should estimate formally the performance of your classifier using accuracy 
(TN + TP)/(TN + TP + FN + FP). Hint: picking articles with COVID-19 keyword in titles/abstracts 
would seed your training set of ‘positive’ texts whereas pre-2020 papers can be taken as the ‘negative’ 
set.
Using the classifier, estimate the proportion of papers on COVID-19 in your dataset:
- As proportion of all papers in 2020 in the dataset you downloaded.
- As proportion of articles in a given journal (e.g. Lancet, Nature) in 2020.

Extract the Named Entities - in most cases these will correspond to names of proteins, genes and medical 
conditions. Since this is a special case of NER you can see an example library here: 
http://www.nactem.ac.uk/GENIA/tagger/. 

Describe briefly in your final report what the algorithm is doing, beyond simply stating the library you used. Based on the Named Entities analyze what are the most commonly mentioned Named Entities with respect to COVID-19
