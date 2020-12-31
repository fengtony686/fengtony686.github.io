---
layout:     post
title:      Artificial Intelligence Poster Session
subtitle:   More Information about Our Work
date:       2020-12-31
author:     Tony Feng
header-img: img/economy.jpg
catalog: true
tags:
    - 论文
    - 学习
    - CS
---

# Introduction

There are two ways to implement AI, one is to translate the knowledge we have directly into an algorithm, and the other is to use a model with learning capabilities using a selected dataset to allow the machine to learn the knowledge on its own. For natural language processing problems, the latter is the popular way of implementation. However, to get a good model trained on a dataset, it is necessary to make the selected dataset as close to the actual problem as possible, or in the wild. However, as we see in the image below, machine learning models can be misled by the imbalance of the dataset (and indeed humans can make similar mistakes).

![intro.png](https://p.sda1.dev/0/ee39265071af1821e6146f7d68e8c75b/intro.png)

Methods have been proposed to remove the misleading effect of writing style and the number of sentence occurrences on the model. Our work focuses on the ways in which the presence or absence of certain neutral words can affect the model's predictions, and how to remove this effect (sometimes misleading).

# Causal Explanation

Firstly, we propose some assumptions to model this problem. Suppose $\mathcal{D}=\mathcal{X}\times\mathcal{Y}$ is the distribution of reviews and labels in reality. $\mathcal{I}$ is the distribution of sampling intention and $\mathcal{S}$ is the distribution of sampling strategy, which is related to the existence of some typical virtual words in this problem. Each time, we take out an element $(x,y,i,s)$ from $\mathcal{A}=\mathcal{X}\times\mathcal{Y}\times\mathcal{I}\times\mathcal{S}$. If $y=i$, then we add this element into $D$. Otherwise, we do not add it into the dataset. Here, $i=1$ means that the annotator wants a positive label, and $i=0$ means that the annotator wants a negative one. From this process, the dataset is created. We need to notice that this is the practical dataset creating process in many situations, so this assumption is reasonable. After the sampling process, suppose the biased distribution is $\overline{\mathcal{A}}$, then we have $P_{\overline{\mathcal{A}}}(X,Y,L)=P(X,Y,L|S=Y)$.

Moreover, it is natural that the sampling intention is completely determined by the sampling strategy. Actually, we assume that the annotator select data purposefully. Therefore, we have the following equation: $P(I|S)=P(I|S,X,Y)$.

Also, it is natural that the label is independent of our sampling strategy (in our problem, the sampling strategy is completely determined by some features in $X$), which can be represented by $P(Y|S)=P(Y)$.

According to the assumptions we proposed, there are six variables in total. In the original distribution, we have variables $X,Y$ that $Y$ is determined by $X$. The sampling intention variable $I$ is completely determined by sampling strategy $S$ according to $P(I|S)=P(I|S,X,Y)$. Suppose in the biased distribution $\overline{\mathcal{A}}$, $X,Y$ are transformed into $\overline{X},\overline{Y}$. Therefore, $\overline{X}$ is determined by $I$ and $X$ while $\overline{Y}$ is determined by $Y$. In our problem, the sampling strategy is related to some virtual words (i.e. the reviewer is used to using 'this' when giving positive reviews), therefore, $S$ is determined by $X$. According to these analysis, the final causal diagram is shown in the figure below. The dataset we see fits the distribution of variables in the red box. The bias of the dataset comes from the green path $X\rightarrow S\rightarrow I\rightarrow \overline{X}$, which changes the distribution of $X$, so that the relationship between $\overline{X}$ and $\overline{Y}$ is not exactly the same as the relationship between $X$ and $Y$.

![causal_diagram.png](https://p.sda1.dev/0/b190358f52e83a85aabf05a320c1bbb1/causal_diagram.png)

Further, we assume that the relationship between $X$ and $Y$ in nature is $Y=f(X)$, and we want to fit $f$ with a machine learning model $f'$. Moreover, the sampling strategy $S$ is determined by a part of $X$ which is shaped as $[word\in sentence]$ in our problem and is denoted as $X''$. All we have to do is to extract $X''$ and use some method (we chose random forest) to estimate the relationship between sampling strategy and sampling intention.

See poster (address at the end of the article) for the specific weights assignment method.

# More Experimental Results

![f1-score](https://p.sda1.dev/0/e899fd370eb4ac2f95c08ffe722fda87/F1-score.png)

The above image shows the F1-scores of the two models before and after the debiasing on the three datasets, and we can see that the model after the debiasing clearly performs better, which indicates that the debiased model generalizes better. However, this is not enough to show that we have successfully removed the model bias caused by the presence or absence of neutral words, so we have completed another experiment. This experiment looked at the change in model prediction by replacing neutral words with unit vectors from word2vec. Admittedly, this setting introduces structural changes to the sentences, but we argue here that the effect on sentence structure is negligible for sentiment analysis tasks.

# References

[1] ZHANG G, BAI B, LIANG J, et al. Selection Bias Explorations and Debias Methods for Natural Language Sentence Matching Datasets[J/OL]. CoRR, 2019, abs/1905.06221. arXiv:1905.06221. http://arxiv.org/abs/1905.06221.

[2] PEARL J. Causality[M]. [S.l.]: Cambridge university press, 2009.

[3] Utagh. IMDB Review Dataset[EB/OL]. 2020. https://www.kaggle.com/utathya/imdb-review-dataset.

[4] Kaggle. Bag of Words Meets Bags of Popcorn[EB/OL]. 2020. https://www.kaggle.com/c/word2vec-nlp-tutorial.

[5] Liu J. 515K Hotel Reviews Data in Europe[EB/OL]. 2020. https://www.kaggle.com/jiashenliu/515k-hotel-reviews-data-in-europe.

[6] VICTOR V, DHANYA S, DAVID B. Using Text Embeddings for Causal Inference[J/OL]. CoRR, 2019, abs/1905.12741. arXiv:1905.12741. http://arxiv.org/abs/1905.12741.

# Poster Address

[**Download PDF**](https://fengtony686.github.io/essay/ai_project_poster.pdf) (Please wait for a few seconds)

[**BibTex**](https://fengtony686.github.io/essay/ai_project_poster.txt)
