# Echo Chambers in Bluesky Starter‑Packs  
_A community‑detection study using Leiden modularity & Infomap_

---

## Project snapshot
I analyse Bluesky “starter‑packs” to test how tightly‑knit clusters (echo chambers) form and how strong their internal consensus is.  
Two complementary algorithms are applied:

* **Leiden modularity** – topology‑driven, coarse partitions  
* **Infomap** – flow‑driven, fine‑grained partitions (random‑walk coding)

Both are evaluated against degree‑preserving null models for statistical significance.

---

## Research Hypotheses

| ID  | Hypothesis statement |
|-----|----------------------|
| **H1** | *Starter packs as seed structures amplify in‑group cohesion and simultaneously reinforce social fragmentation by concentrating interactions within well‑defined user clusters.* |
| **H2** | *Interaction networks within specific starter packs exhibit echo‑chamber characteristics, with high reciprocity and topical homogeneity reinforcing internal consensus.* |
| **H3** | *Structural bias exists inside starter packs, reinforcing hierarchical dominance of certain identity groups through uneven centrality and assortative connectivity.* |
| **H4** | *Political Science and STEM (Natural Science) users display different levels of intellectual openness, as measured by cross‑starter‑pack interaction rates.* |

---

## Key dependencies used

| Package          | Version (tested) | Purpose                                   |
|------------------|------------------|-------------------------------------------|
| `networkx`       | 3.2.1            | Build directed interaction graphs         |
| `python‑igraph`  | 0.11.x           | Fast graph backend                        |
| `leidenalg`      | 0.10.x           | Leiden community detection                |
| `scikit‑learn`   | 1.4.x            | Normalized Mutual Information (NMI)       |
| `matplotlib`     | 3.8.x            | All plots                                 |
| `numpy`          | 1.26.x           | Stats + null‑model simulation             |

The network visuals throughout the paper were prepared and designed in **Gephi**.

---

## Results at a glance

| Network theme      | Leiden \(Q_{\text{real}}\) | Null mean | p‑value  | Infomap avg NMI |
|--------------------|---------------------------|-----------|----------|-----------------|
| Natural Science    | 0.556 (bin) / 0.568 (w)   | 0.19 / 0.20 | < 0.0001 | 0.964 |
| Political Science  | 0.406 (bin) / 0.407 (w)   | 0.146 / 0.156 | < 0.0001 | 0.925 |

Both methods confirm statistically strong internal clustering (supports **H2**).

---

## 📝 How to cite
Dilbaz M. et al. 2025  
*Echo Chambers in Bluesky Starter‑Packs: A Community‑Detection Study.*  
<https://github.com/your‑handle/bluesky‑echo‑chambers>

---

*This README only describes the parts **I actually built and tested myself** (data‑frame creation, graph building, Leiden modularity, Infomap, and null‑model evaluation).  
Feel free to adapt wording as needed.*
