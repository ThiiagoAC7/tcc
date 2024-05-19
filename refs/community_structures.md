# Near linear time algorithm to detect community structures in large-scale networks.pdf

## TODO:
    - [] review section 2
    - [] review section 3

## Networks
- Social networks are represented by people and as nodes and their relationship as edges
- Finding community structures in networks is another step toward understanding
the complex systems they represent
- **A Community in a Network** 
    - group of nodes that are similar to each other and dissimilar from the rest of the 
    network

## Community
- There is no university accepted definition for a community, but is well known
that most real-world networks display community structures
- **Community Detection Algorithm**
    - goal: find groups of nodes of interest in a given network.
    - finds groups that either have an inherent or an externally specified notion of 
    similarity among nodes within groups
    - number of communities and their sizes are not known beforehand.
    - localized community detection algorithm based on label propagation
- communities in social networks can provide insights about common characteristics or
beliefs among people that makes them different from other communities
- strength of communities :
    - definition based on degrees (number of edges)
    - comparing the density of edges in the network as a whole
    - ***Label Flooding algorithms***:
        - a node is intialized with a label wich then propagates step by step 
        via the neighbors until it reaches the end of the community

### Community Detection using Label Propagation

- Node X has neighbors X1, X2, ..., Xn
- each neighbor carries a label denoting wich community they belong
- X determines its community based on the labels of its neighbors
- each node is initialized with a unique label, and the labels propagate through the 
network
- densely connected groups quickly reach a consensus on a unique label
    - they continue expanding outwards until it is possible to do so 
- stop criterion is similar to the definition of strong communities


# Detection and Analysis of Fake News Users’ Communities in Social Media

Community detection is a valuable tool that can help identifying clusters or communities within
a social network, providing insights into the structure and function of the whole network

-The most popular four common unsupervised algorithms for community detection are the following.
    1. The Louvain Algorithm [13]: It seeks to optimize a
    quality function and operates in two steps. In the first
    step, nodes are moved to a selected community in a way
    that gives the best increase in the quality function. In the
    second step, communities are represented as individual
    nodes, and the process is repeated until the quality of
    the function can no longer be increased.
    2. Infomap [14]: It uses the code length of a random walk
    of the map as the objective to be optimized, in order
    to detect the network structure. Infomap is based on the
    map equation, a method that models a flow as random
    walks through the graphs and a graph partitioning is
    scored by finding a compressed modular representation
    of this flow.
    3. LPA [15]: It is a fast community detection algorithm
    that uses the network’s structure as a guide. Each node is
    assigned a specific label. Afterward, an iterative process
    of label propagation is applied, whereby a node’s label
    is set as the most common label among its neighbors.
    The process stops when no labels are updated for all the
    nodes. LPA can also apply semi-supervised learning by
    initially assigning some nodes to communities.
    4. The Girvan–Newman Algorithm [16]: It is based on the
    idea that nodes are strongly connected within the same
    community and loosely connected to nodes from other
    communities. To identify these groups, the algorithm
    removes edges with the most number of shortest paths
    between nodes. This process breaks down the network
    into distinct communities.
