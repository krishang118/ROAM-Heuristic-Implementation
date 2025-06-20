# ROAM Heuristic Implementation (Strategic Social Networks)

This repository presents a from-scratch implementation of the ROAM (Remove One, Add Many) heuristic for a 'strategic social network', based on the 2017 research paper:

> **"Strategic Social Network Analysis"** by Tomasz Michalak, Talal Rahwan, and Michael Wooldridge ([AAAI 2017](https://aaai.org/papers/11142-aaai-31-2017/)).

## Research Paper Context

The paper introduces a new paradigm for social network analysis that explicitly models the strategic behavior of network actors. It addresses questions such as how individuals or groups can evade detection by social network analysis tools, and how such tools can be made robust to strategic manipulation. The ROAM heuristic is one such strategy, allowing a network leader to rewire connections to reduce their detectability while maintaining network functionality.

## Implementation

The main implementation is in the Jupyter notebook:
- `ROAM Heuristic.ipynb`.

This notebook:
- Loads a real-world terrorist network dataset (Madrid train bombings, 2004).
- Computes classic centrality measures (degree, closeness, betweenness).
- Identifies the network leader.
- Applies the ROAM heuristic to simulate strategic evasion.
- Analyzes and visualizes the effect on the leader's centrality and influence.

## Dataset

The dataset is available at [Netzschleuder](https://networks.skewed.de/net/train_terrorists). It contains:
- **nodes.csv**: Node list (each node is a suspected terrorist, with 2D position for visualization)
- **edges.csv**: Edges (connections between individuals, with weights encoding connection strength)
- **gprops.csv**: Metadata and citation info

**Description:**
> A network of associations among the terrorists involved in the 2004 Madrid train bombing, as reconstructed from press stories after-the-fact. Edge weights encode four levels of connection strength: friendships, ties to Al Qaeda and Osama Bin Laden, co-participants in wars, and co-participants in previous terrorist attacks.

## How to Run

1. Clone this repository on your local machine.
2. Unzip the dataset file.
3. Run and execute the Jupyter Notebook.

## References
- Michalak, T., Rahwan, T., & Wooldridge, M. (2017). [Strategic Social Network Analysis](https://aaai.org/papers/11142-aaai-31-2017/). AAAI Conference on Artificial Intelligence.
- [Netzschleuder: train_terrorists dataset](https://networks.skewed.de/net/train_terrorists)

## Contributing

Contributions are welcome!

## License

Distributed under the MIT License.
