# Data-Structure
2025.03.28
#### 1. Let G be a weighted, undirected, connected graph with unique edge weights. Prove that G has a unique MST.
assume there are 2 such MST, MST1, MST2, MST1 中有e1 as minimum weight, 不在MST2中。 在MST2 中添加e1， MST2'有一个circle，MST2' 不可能此时在MST1中，因为1是tree，不包括Circle(也必有e2不在1中)
#### Let B∗ = B + e1 − e2. In other words, B∗ is the spanning tree obtained by adding e1 to B and removing e2 from B. Since w(e1) − w(e2) < 0, the sum of the weights of edges in B∗ is less than the sum of the weights of edges in B. So B∗ is a spanning tree of G with less weight than B. Therefore, B is not a MST of G, contradicting the definition of B
