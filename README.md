# Supplemental material for paper: "Fair-mod: Fair Modular Community Detection"
Supplemental material for paper "Fair-mod: Fair Modular Community Detection", to be published in the proceedings for Complex Networks and their Applications 2024. Publication available here: [https://link.springer.com/chapter/10.1007/978-3-031-82435-7_8](https://link.springer.com/chapter/10.1007/978-3-031-82435-7_8). See also pre-pub in the main folder of this repository.

This repository contains the implementation of the Fair-mod modularity-based community detection algorithm, with a weighted balance-based fairness. The implementation is based on the source code for Louvain community detection found in the NetworkX library, see source code here: (https://networkx.org/documentation/stable/_modules/networkx/algorithms/community/louvain.html). 

If you use Fair-mod to support your research, consider citing:
> Panayiotou, G., Magnani, M. (2025). *Fair-mod: Fair Modular Community Detection*.  
> In: Cherifi, H., Donduran, M., Rocha, L.M., Cherifi, C., Varol, O. (eds) *Complex Networks & Their Applications XIII*.  
> COMPLEX NETWORKS 2024. Studies in Computational Intelligence, vol 1189. Springer, Cham.  
> [https://doi.org/10.1007/978-3-031-82435-7_8](https://doi.org/10.1007/978-3-031-82435-7_8)

## Usage
The algorithm expects as input a NetworkX graph object. The graph should be undirected (directed graphs are not currently supported), and the sensitive attribute S for the graph should be coded as a node attribute named `color`, taking either of two values: `red` or `blue`. Future versions will address the limitations of the implementation.

The repository also includes:
* `process_raw.py`: Code to process the raw social network datasets featured in the paper, generating the desired NX objects.
* `s_fair_sc.py`: Code for the Scalable Fair Spectral Clustering (sFairSC) algorithm, translated from the original MATLAB version of the code in https://github.com/jiiwang/scalable_fair_spectral_clustering. Credit for the algorithm goes to the original authors:

<a id="1">[1]</a> 
Ji Wang et al. (2023).
Scalable Spectral Clustering with Group Fairness Constraints.
Proceedings of The 26th International Conference on Artificial Intelligence and Statistics.

