Topic-Modeling-Case-Study-Local.zip contains the data and the notebooks that you can open locally
using a Jupyter server. Alternatively, Topic-Modeling-Case-Study-WS.zip is a zip archive file
containing the files needed to complete this study case in Watson Studio. 



The topic_modeling-case-study notebook will provide code snippets and instructions for the
exercises. We strongly encourage that you try the exercises on your own before referring to the
solutions notebook ​provided at the end of the case study.

Guiding principle for the case study

Topic modeling is a commonly used form of dimensionality reduction. When we use visualization
tools to explore the results of topic modeling one strong hope is that we can identify features
that are relevant to the domain. These insights can be in turn be transformed into new features
that then can be used directly or appended to the feature matrix. We use topic modeling in this
case study to enables domain specific feature engineering.

We will use the benchmark dataset movie reviews dataset [1]. The case study will make use of the
NLTK package and you will want to ensure that you have run the following either as part of your
notebook or at some point before.

Note: IBM Watson Natural Language Understanding, Natural Language Classifier, and Watson Discovery
make use of pre-trained models for many different use cases. They may also be custom trained for
specific knowledge domains.
```
import nltk
nltk.download('all')
```

The visualization of topics in a large corpus can be challenging. We will use the software
pyLDAvis that integrates directly into Jupyter notebooks. This is based on the LDAvis project [2]. 
To install it use: 

```
pip install pyldavis 
```
[[1]](http://ai.stanford.edu/~amaas/data/sentiment/)
[[1]](https://www.aclweb.org/anthology/P11-1015/)
[[2]](https://www.researchgate.net/publication/265784473_LDAvis_A_method_for_visualizing_and_interpreting_topics?channel=doi&linkId=541affaf0cf25ebee988df72&showFulltext=true)
[[2]](https://nlp.stanford.edu/events/illvi2014/papers/sievert-illvi2014.pdf)