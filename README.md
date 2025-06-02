# ROAM Heuristic Implementation (Strategic Social Network)

This repository contains an implementation of the ROAM (Remove One, Add Many) heuristic for strategic social network analysis, based on the 2017 research paper:

> **"Strategic Social Network Analysis"** by Tomasz Michalak, Talal Rahwan, and Michael Wooldridge ([AAAI 2017](https://aaai.org/papers/11142-aaai-31-2017/))

## Research Paper Context

The paper introduces a new paradigm for social network analysis that explicitly models the strategic behavior of network actors. It addresses questions such as how individuals or groups can evade detection by social network analysis tools, and how such tools can be made robust to strategic manipulation. The ROAM heuristic is one such strategy, allowing a network leader to rewire connections to reduce their detectability while maintaining network functionality.

## Implementation

The main implementation is in the Jupyter notebook:
- `ROAM Heuristic.ipynb`

This notebook:
- Loads a real-world terrorist network dataset (Madrid train bombing, 2004)
- Computes classic centrality measures (degree, closeness, betweenness)
- Identifies the network leader
- Applies the ROAM heuristic iteratively to simulate strategic evasion
- Analyzes and visualizes the effect on the leader's centrality and influence

## Dataset

The dataset is from the [KONECT collection](http://konect.cc/networks/moreno_train) and is also available at [Netzschleuder](https://networks.skewed.de/net/train_terrorists):
- **nodes.csv**: Node list (each node is a suspected terrorist, with 2D position for visualization)
- **edges.csv**: Edges (connections between individuals, with weights encoding connection strength)
- **gprops.csv**: Metadata and citation info

**Description:**
> A network of associations among the terrorists involved in the 2004 Madrid train bombing, as reconstructed from press stories after-the-fact. Edge weights encode four levels of connection strength: friendships, ties to Al Qaeda and Osama Bin Laden, co-participants in wars, and co-participants in previous terrorist attacks.

**Citation:**
```
@article{konect:hayes,
  title = {Connecting the Dots. Can the Tools of Graph Theory and Social-network Studies Unravel the Next Big Plot?},
  author = {Hayes, Brian},
  journal = {Am. Scientist},
  volume = {94},
  number = {5},
  pages = {400--404},
  year = {2006},
}
```

## How to Run

1. **Install dependencies:**
   - Python 3.10+
   - Recommended: Use a virtual environment
   - Install required packages:
     ```bash
     pip install pandas numpy networkx matplotlib seaborn
     ```
2. **Open the notebook:**
   - Launch Jupyter Notebook or JupyterLab
   - Open `ROAM Heuristic.ipynb`
3. **Run all cells:**
   - The notebook will load the data, perform the analysis, and display results/plots.

## Dependencies
- pandas
- numpy
- networkx
- matplotlib
- seaborn

## References
- Michalak, T., Rahwan, T., & Wooldridge, M. (2017). [Strategic Social Network Analysis](https://aaai.org/papers/11142-aaai-31-2017/). AAAI Conference on Artificial Intelligence.
- Hayes, B. (2006). Connecting the Dots: Can the tools of graph theory and social-network studies unravel the next big plot? *American Scientist*, 94(5), 400-404.
- [KONECT: Koblenz Network Collection](http://konect.cc/networks/moreno_train)
- [Netzschleuder: train_terrorists dataset](https://networks.skewed.de/net/train_terrorists)

---

For questions or academic use, please cite the original paper and dataset as above. 
