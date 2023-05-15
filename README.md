# Graph.pNG
constraints on primordial non-gaussianity using GNNs (IMNN and regression techniques)

- [Github Repo](https://github.com/tlmakinen/graphPNG)

Simulations: *Quijote-PNG*
- [paper 1](https://arxiv.org/pdf/2206.01624.pdf)
- [paper 2](https://arxiv.org/pdf/2206.15450.pdf)


What sort of constraints can we obtain following the analysis in [the Cosmic Graph](https://arxiv.org/abs/2207.05202v3) paper with gIMNNs ?

## basic proof-of-concept setup

**Input graphs:**

- fixed mass cut on known masses (yields $\approx$ 200 DM halos per simulation)
- fixed connection length of $r_{\rm connect}=200\ \rm Mpc$
- rotationally- and translationally-invariant coordinate system (stored in edges)

**GNN setup:**
- simple MLP models for node, edge, and global functions
- multi-head aggregation function for nodes and edges: $\bigoplus_i \in [\rm sum, mean, var, max]$
- $2\times$ GNN Blocks:
    1. edge update
    2. node update
    3. global update
