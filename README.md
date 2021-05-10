# Graph Mincuts UGP

This Undergraduate Project was completed in two parts at Indian Institute of Technology, Kanpur for partial fulfilment of my degree. The project was completed under the supervision of Prof Surender Baswana, Department of Computer Science and Engineering. 

- CS498 (Semester 2020-21 I) : Fault-Tolerant All-Pairs Mincuts
- CS396 (Sememster 2020-21 II) : Sensitivity Oracle for All-Pairs Mincuts, also includes Lower Bounds for Mincut Data Structures.

## Part 1: Fault-Tolerant All-Pairs Mincuts

Link - https://arxiv.org/pdf/2011.03291.pdf

Let G=(V,E) be an undirected unweighted graph on n vertices and m edges. We address the problem of fault-tolerant data structure for all-pairs mincuts in G defined as follows.

Build a compact data structure that, on receiving a pair of vertices s,t∈V and any edge (x,y) as query, can efficiently report the value of the mincut between s and t upon failure of the edge (x,y).

To the best of our knowledge, there exists no data structure for this problem which takes o(mn) space and a non-trivial query time. We present two compact data structures for this problem.
- Our first data structure guarantees O(1) query time. The space occupied by this data structure is O(n2) which matches the worst-case size of a graph on n vertices.
- Our second data structure takes O(m) space which matches the size of the graph. The query time is O(min(m,ncs,t)) where cs,t is the value of the mincut between s and t in G. The query time guaranteed by our data structure is faster by a factor of Ω({\sqrt n}) compared to the best known algorithm to compute a (s,t)-mincut.


## Part 2: Sensitivity Oracle for All-Pairs Mincuts

Let G=(V,E) be an undirected unweighted graph on n vertices and m edges. We address the problem of sensitivity oracle for all-pairs mincuts in G defined as follows.

Build a compact data structure that, on receiving a pair of vertices s,t∈V and insertion/deletion of any edge as query, can efficiently report the value of the mincut between s and t upon the update.

To the best of our knowledge, there exists no data structure for this problem which takes o(mn) space and a non-trivial query time. Recently, Baswana, Gupta, and Knollman gave a data structure that can handle single edge insertion in O(n^2) space and O(1) query time. We present the following results.

- We present a sensitivity oracle for all-pairs mincuts. Our data structure guarantees O(1) query time. The space occupied by this data structure is O(n^2) which matches the worst-case size of a graph on n vertices. A resulting (s,t)-mincut after edge insertion/deletion can be reported in O(n) time which is optimal. Our data structure also subsumes the results of Baswana, Gupta, and Knollman.
- We give conditional lower bounds on data structures that can handle dual-deletions (or dual-faults) for a (s,t)-mincut. We also give a conditional lower bound on a data structure storing all static ({s,u},{t,v})-mincut values with fixed s,t∈V. This implies a conditional lower bound for a generalized flow tree for 2x2 mincuts, i.e. a data structure that can report the value of static ({s,u},{t,v})-mincut for given vertices s,t,u,v∈V.

Some parts of this work have been taken from a recent research of Baswana and Pandey, but presented here for sake of continuity. 


For citation of Part 1, the following may be used.
```
@article{DBLP:journals/corr/abs-2011-03291,
  author    = {Surender Baswana and
               Abhyuday Pandey},
  title     = {Fault-Tolerant All-Pairs Mincuts},
  journal   = {CoRR},
  volume    = {abs/2011.03291},
  year      = {2020},
  url       = {https://arxiv.org/abs/2011.03291},
  archivePrefix = {arXiv},
  eprint    = {2011.03291},
  timestamp = {Thu, 12 Nov 2020 15:14:56 +0100},
  biburl    = {https://dblp.org/rec/journals/corr/abs-2011-03291.bib},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}
```
