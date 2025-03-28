# Data-Structure
2025.03.28
#### 1. Let G be a weighted, undirected, connected graph with unique edge weights. Prove that G has a unique MST.
assume there are 2 such MST, MST1, MST2, MST1 中有e1 as minimum weight, 不在MST2中。 在MST2 中添加e1， MST2'有一个circle，MST2' 不可能此时在MST1中，因为1是tree，不包括Circle(也必有e2不在1中)
#### Let B∗ = B + e1 − e2. In other words, B∗ is the spanning tree obtained by adding e1 to B and removing e2 from B. Since w(e1) − w(e2) < 0, the sum of the weights of edges in B∗ is less than the sum of the weights of edges in B. So B∗ is a spanning tree of G with less weight than B. Therefore, B is not a MST of G, contradicting the definition of B
#### 2. bipartite if and only if it is possible to partition its vertices into two sets so that all edges have one endpoint in each set. That is, there exist two non-empty subsets V1, V2 of V such that V1∪V2 = V , V1 ∩ V2 = ∅, and all edges in E have one endpoint in V1 and another one in V2.（二分图）
We make use of the fact that a graph is bipartite graph iff it has no odd-cycle.（判断每两个vertex直接是odd or even）
BIPARTITE(G):
    pick s an element in V(G)
    BFS(G,s) # run BFS and for each vertex keep the distance from s
    for each (u,v) in E(G):
      if (u.d-v.d) mod 2 == 0:
        return FALSE
    return TRUE
#### runtime : running time of BFS is O(|E| + |V |) = O(|E|), since |E| ≥ |V | − 1 for connected graphs, and therefore the algorithm BIPARTITE runs in time Θ(|E|).
