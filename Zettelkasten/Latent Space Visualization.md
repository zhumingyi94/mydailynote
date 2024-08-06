**202408060959**
**Status:** #flashcards #machinelearning #visualization 
**Tags: ** 
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

# Latent Space Visualization
<hr style="border: none; height: 2px; background-color: #000000; margin: 20px 0;">

### Key note
#### <font color="#0070c0">PCA</font>
$Cov(X) = \frac{1}{n}X^T$ 
$Cov(X)v = \lambda v$
Complexity = $O(nd^2+d^3)$

When use to visualize latent space of auto encoder -> get the eigenvalue information 
**Not work well with non-linear data**. Why ? 
#### <font color="#0070c0">t-SNE</font>
t-Distributed Stochastic Neighbor Embedding (der Maaten & Geoffrey Hinton)
"Point that are close to each other in higher dimension should be closer when projected into low dimensional space"

$$ \frac{ \partial \text{Loss(HighDim, LowDim)} }{ \partial \text{LowDim} }$$
![[Pasted image 20240806102321.png]]
Turn distances between points and neighbor to probability distribution 
Perplexity - You have to try different value until you're satisfied 

t-SNE: 
- Gaussian: Higher space
- t distribution: Lower space
#### <font color="#0070c0">UMAP</font>
Uniform Manifold Approximation and Projection 
Topology + Categorical theory (I die at this point)
Using Graph for both
### Exercise


### References

