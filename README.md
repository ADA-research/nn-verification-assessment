The companion repository to the paper 

**Critically Assessing the State of the Art in Neural Network Verification**, Matthias König, Annelot W Bosman, Holger H Hoos, Jan N van Rijn, *published at JMLR*. 

**Abstract:** Recent research has proposed various methods to formally verify neural networks against minimal input perturbations; this verification task is also known as local robustness verification. The research area of local robustness verification is highly diverse, as verifiers rely on a multitude of techniques, including mixed integer programming and satisfiability modulo theories. At the same time, the problem instances encountered when performing local robustness verification differ based on the network to be verified, the property to be verified and the specific network input. This raises the question of which verification algorithm is most suitable for solving specific types of instances of the local robustness verification problem. To answer this question, we performed a systematic performance analysis of several CPU- and GPU-based local robustness verification systems on a newly and carefully assembled set of 79 neural networks, of which we verified a broad range of robustness properties, while taking a practitioner's point of view -- a perspective that complements the insights from initiatives such as the VNN competition, where the participating tools are carefully adapted to the given benchmarks by their developers. Notably, we show that no single best algorithm dominates performance across all verification problem instances. Instead, our results reveal complementarities in verifier performance and illustrate the potential of leveraging algorithm portfolios for more efficient local robustness verification. We quantify this complementarity using various performance measures, such as the Shapley value. Furthermore, we confirm the notion that most algorithms only support ReLU-based networks, while other activation functions remain under-supported.

This repository provides

- the performance data collected for this study;
- the neural networks, which were verified.

**Note:** The ground truth of each instance cannot be known a priori. In some cases, the verifiers returned different solutions (i.e. one verifier found a given instance to be *sat* whereas another found it to be *unsat*). We observed this specifically among GPU-based methods. In our analysis, we treated these instances as *unsat* as we did not investigate the validity of the counterexample if any was found.

Citation:
```
@article{KonEtAl24b,
    author = {K{\"o}nig, Matthias and Bosman, Annelot W and Hoos, Holger H and van Rijn, Jan N},
    title = "Critically Assessing the State of the Art in Neural Network Verification",
    journal = "Journal of Machine Learning Research",
    year = "2024",
    volume = "25",
    number = "12",
    pages = "1--53"
}
```
