Using PubMed trained Word2Vec word embeddings to see 
if known gene-disease relationships are reliably 
encoded in vector space. Code in this directory is 
forked  from
https://github.com/spyysalo/wvlib but TBH the command line interface 
to do this analysis was an early
idea that I basically abonded.  Instead I started a notebook
"Vector similarity.ipynb" which does the analogy task in demo form.

The embeddings I used came from http://evexdb.org/pmresources/vec-space-models/ and are multi-GB files that are not under source code control. You will need to download wikipedia-pubmed-and-PMC-w2v.bin and PubMed-w2v.bin to get the notebook to work locally for you.

 
2020-02-22
jfleischer@ucsd.edu

Original README of the forked project is below this line
===========================

wvlib - word vector library
===========================

Work in progress, not currently recommended for any use.

Try the following:

Find 10 words closest to "protein" using word2vec vectors induced on
the text8 demo data

    echo protein | python nearest.py text8.tar.gz -n 10

Find word that has the same relationship to "japan" as "paris" has
to "france"

    echo 'france paris japan' | python analogy.py text8.tar.gz -q -n 1

Evaluate the vectors on the binary classification task using words
from McIntosh and Curran "Reducing semantic drift with bagging and
distributional similarity" (ACL 2009)

    python evalclass.py text8.tar.gz word-classes/McIC-09/*.txt

Evaluate the vectors on the closed-class member retrieval task
using the set of standard amino acids

    python evalset.py text8.tar.gz word-sets/Ohta-bio-sets/standard-amino-acids.txt

The rest of this README is TODO. See scripts for documentation.
