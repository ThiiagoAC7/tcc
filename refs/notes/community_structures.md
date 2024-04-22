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


