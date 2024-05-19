# Graph Neural Networks

- GNNs are designed to deal with  data generated from non-Euclidean domains.
- GNNs can perform 
    - node regression,
    - node classification, 
    - link prediction, 
    - edge classification 
    - graph classification depending on the requirements.

## Propagation Algorithms 

- label the propagation pattern of each item of news, which is a graph
    - Rex Ying, Jiaxuan You, Christopher Morris, Xiang Ren, William L. Hamilton,
    and Jure Leskovec. 2018. Hierarchical Graph Representation Learning with
    Differentiable Pooling. In Proceedings of the 32nd NIPS. 4805–4815.

-Thomas N. Kipf and Max Welling. 2017. Semi-Supervised Classification with
Graph Convolutional Networks. In Proceedings of the 5th ICLR. Palais des Con-
grÃĺs Neptune, Toulon, France.
- Zonghan Wu, Shirui Pan, Fengwen Chen, Guodong Long, Chengqi Zhang, and
Philip S. Yu. 2019. A Comprehensive Survey on Graph Neural Networks. arXiv
e-prints (2019), arXiv:1901.00596.

## MODEL TRAINING EFFICIENCY

- Model efficiency. When training and testing our models, we
also find that GNNs converge very quickly—most of the time it only
takes dozens of epochs for the model to reach similar performance
to the final model in terms of the four metrics, while each epoch
lasts from only a couple of seconds to several minutes, depending
on the different model structures and sizes of the datasets.
