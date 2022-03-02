# Netflix-recommender-system
Predict movie ratings given movie for each user

To predict rating's loss equation can be formulated as  


![image](https://user-images.githubusercontent.com/48724432/156401565-c94a28be-8ee6-4f39-b705-6224a2edd8c2.png)

μ  : scalar mean rating   
bi : scalar bias term for user i   
cj : scalar bias term for movie j   
ui : K-dimensional vector for user i    
vj : K-dimensional vector for movie j
  
Construct adjacency matrix with the given data, assuming its  <a href='https://en.wikipedia.org/wiki/Bipartite_graph'> weighted un-directed bi-partited graph</a> and the weight of each edge is the rating given by user to the movie

<img src='https://i.imgur.com/rmUCGMb.jpg' width=200>


Applying SVD decomposition on the Adjaceny matrix returns three matrices  U,∑,V  such that  U×∑×VT=A ,
if  A  is of dimensions  N×M  then
U is of  N×k ,
∑  is of  k×k  and
V  is  M×k  dimensions.


predicted(yij) = μ+bi+cj+dot_product(ui,vj)


## Reference/Source

https://datajobs.com/data-science-repo/Recommender-Systems-[Netflix].pdf
