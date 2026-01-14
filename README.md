# Source-Free Domain Adaptation for Geospatial Point Cloud Semantic Segmentation
Official code for  [Source-Free Domain Adaptation for Geospatial Point Cloud Semantic Segmentation](https://arxiv.org/abs/2601.08375v1).

Semantic segmentation of 3D geospatial point clouds is pivotal for remote sensing applications. However, variations in geographic patterns across regions and data acquisition strategies induce significant domain shifts, severely degrading the performance of deployed models. Existing domain adaptation methods typically rely on access to source-domain data. However, this requirement is rarely met due to data privacy concerns, regulatory policies, and data transmission limitations. This motivates the largely underexplored setting of source-free unsupervised domain adaptation (SFUDA), where only a pretrained model and unlabeled target-domain data are available. In this paper, we propose LoGo (Local–Global Dual-Consensus), a novel SFUDA framework specifically designed for geospatial point clouds. At the local level, we introduce a class-balanced prototype estimation module that abandons conventional global threshold filtering in favor of an intra-class independent anchor mining strategy. This ensures that robust feature prototypes can be generated even for sample-scarce tail classes, effectively mitigating the feature collapse caused by long-tailed distributions. At the global level, we introduce an optimal transport-based global distribution alignment module that formulates pseudo-label assignment as a global optimization problem. By enforcing global distribution constraints, this module effectively corrects the over-dominance of head classes inherent in local greedy assignments, preventing model predictions from being severely biased towards majority classes. Finally, we propose a dual-consistency pseudo-label filtering mechanism. This strategy retains only high-confidence pseudo-labels where local multi-augmented ensemble predictions align with global optimal transport assignments for self-training. Extensive experiments on two challenging benchmarks, encompassing cross-scene and cross-sensor settings, demonstrate that LoGo consistently outperforms existing state-of-the-art methods. Notably, LoGo achieves mIoU improvements of 5.9% on the STPLS3D to H3D task and 11.42% on the DALES to T3D task compared to the source-only baseline.


# Note
We will release our code soon.

# Cite
Please cite our work if you find it useful.
```bibtex
@misc{gao2026sourcefreedomainadaptationgeospatial,
      title={Source-Free Domain Adaptation for Geospatial Point Cloud Semantic Segmentation}, 
      author={Yuan Gao and Di Cao and Xiaohuan Xi and Sheng Nie and Shaobo Xia and Cheng Wang},
      year={2026},
      eprint={2601.08375},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2601.08375}, 
}
```
