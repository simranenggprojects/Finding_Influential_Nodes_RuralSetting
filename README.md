# Finding Influential Nodes in Rural Setting
To find highly central individuals in rural village who can diffuse information faster and far.

### Problem Motivation and Introduction
Government launches a lot of schemes for rural India which may be related to education, employment, food and ration, women employment, immunization etc. What do you think makes these schemes scuccessful? Well, you may think it's how good that scheme is, best idea, most successful. Ummm, unfortunately, you answered wrong. Usually very remote rural people are unaware of them and hence howsoever good the scheme is, it won't be successful if it doesn't reach target audience. So it is extremely essential to find highly central individuals who can spread information faster and far.

The traditional methods of PageRank, Degree Centrality, Betweeness Centrality fail to produce good results in rural settings where there are no proper graphs and social networks. Idea of our proposed algorithm is to jointly learn community detection with finding influential nodes.

### Dataset
Link: https://dataverse.harvard.edu/file.xhtml?persistentId=doi:10.7910/21538/4POS1J&version=9.4
Villages taken into consideration: Village 2 and Village 11 (referred as Vil 1 here in ppt and report)

### Baselines
* Degree Centrality
* Closeness Centrality
* Betweeness Centrality
* PageRank
* Katz Centrality

### Proposed Solution
1. To get the latent representations of the nodes, apply DeepWalk.
2. Apply K-Means clustering to detect the communities. (K = no. of clusters = no. of nodes to be selected for information diffusion)
3. Find central node (using PageRank) from community and then report them as initial seed nodes.
4. Model the information flow through general threshold model.

### Results
Average 2.3% increase in the number of nodes infected as compared to the best performing baseline.
