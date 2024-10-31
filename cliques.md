# Coordinated Inauthentic Behaviour


In the network analysis portion of the methodology for characterizing coordinated inauthentic 
behavior on YouTube, the approach can be broken down into the following key steps:

## Co-commenter Network Construction:
A network is built for each YouTube channel where commenters are represented as nodes, and edges 
(connections) are established between pairs of commenters who comment on the same videos. 
This helps reveal potential coordination among users.
To filter out noise, only commenter pairs who co-commented on at least 10 videos were retained.

## Network Features Extraction:
Several structural metrics are computed for these co-commenter networks, including:
- Average Degree: A measure of the average number of connections each node (commenter) has.
- Number of Nodes and Edges: These metrics represent the size of the network and the total number 
of connections between commenters, respectively.
- Clustering Coefficient: This measures how connected a node’s neighbors are to one another, which 
can reveal the tightness of groups or clusters within the network.
- Modularity: A metric that assesses the degree to which the network is divided into smaller, tightly 
connected subgroups, useful for identifying community structures.

1. Clique Analysis:
- Maximal Cliques: A clique is a subset of nodes that are all directly connected to each other. 
Maximal cliques are those that cannot be expanded by including additional adjacent nodes. 
Channels with larger and more frequent cliques may signal coordinated behavior.
- Features such as the average degree of clique members and the comparison of clique-based metrics 
with the overall network are also computed to identify suspiciously tight-knit groups.

2. Correlation and Clustering:
- After computing the network and clique-based features, a similarity analysis is performed using 
Pearson correlation coefficients to examine relationships between different features.
- Principal Component Analysis (PCA) and clustering techniques like k-means or hierarchical 
clustering are applied to group YouTube channels based on the extracted network features, which 
helps identify clusters of channels that may be exhibiting coordinated inauthentic behavior.

3. Suspicious Behavior Detection:
- Channels showing significant coordination in their co-commenter networks (e.g., high clique sizes 
or high modularity) are flagged as potentially suspicious. By analyzing these features, patterns of 
coordinated behavior across multiple channels can be detected and grouped.

This network analysis helps uncover clusters of channels that engage in coordinated behavior, 
enabling researchers to detect manipulation and inauthentic engagement.
