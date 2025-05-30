# Persistent homology for Russian and Slovenian words and bigrams

This repository contains the code related to computing persistent homology for four semantic spaces:
-  Russian words
-  Slovenian words
-  Russian bigrams
-  Slovenian bigrams
The work is a part of HSE research paper supervised by Gromov V.A.


## Pipeline

``bigram_embeddings.ipynb`` → get dictionaries and embeddings of bigrams based on corpora and  trained word embeddings ([source code for WE](https://github.com/VTermus/slv_embeddings))
``pca_clustering_partition.ipynb`` → reduce dimension of vector spaces using pca for visualisations; clusterize using k-means and split space into parts
``Julia_homology.ipynb`` → compute h0 and h1 persistent homologies for each part of each vector space using [Ripserer.jl](https://github.com/mtsch/Ripserer.jl) package
``filter_holes_words.ipynb``, ``filter_holes_bigrams.ipynb`` → find the most persistent h1 homologies based on hole features and identify hole contours


## Results

``space partition`` → clusterization and space split resuls
homology → h0, h1 vectors and lifetimes, hole indices
``holes filtered`` → h1 homologies filtered by lifetimes and hole diameters 
``hole contours`` → words and bigrams on the contours of the most persistent holes 
