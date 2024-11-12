# awesome-4D-reconstruction

A curated list of papers and open-source resources focused on 4D reconstruction model. 

### 1. [CVPR '2021] D-NeRF: Neural Radiance Fields for Dynamic Scenes
**Authors**: Albert Pumarola, Enric Corona, Gerard Pons-Moll, Francesc Moreno-Noguer
<details span>
<summary><b>Abstract</b></summary>
  Neural rendering techniques combining machine learning with geometric reasoning have arisen as one of the most promising approaches for synthesizing novel views of a scene from a sparse set of images. Among these, stands out the Neural radiance fields (NeRF), which trains a deep network to map 5D input coordinates (representing spatial location and viewing direction) into a volume density and view-dependent emitted radiance. However, despite achieving an unprecedented level of photorealism on the generated images, NeRF is only applicable to static scenes, where the same spatial location can be queried from different images. In this paper we introduce D-NeRF, a method that extends neural radiance fields to a dynamic domain, allowing to reconstruct and render novel images of objects under rigid and non-rigid motions from a \emph{single} camera moving around the scene. For this purpose we consider time as an additional input to the system, and split the learning process in two main stages: one that encodes the scene into a canonical space and another that maps this canonical representation into the deformed scene at a particular time. Both mappings are simultaneously learned using fully-connected networks. Once the networks are trained, D-NeRF can render novel images, controlling both the camera view and the time variable, and thus, the object movement. We demonstrate the effectiveness of our approach on scenes with objects under rigid, articulated and non-rigid motions.
</details>

  [📄 Paper](https://arxiv.org/pdf/2011.13961) | [💻 Code](https://github.com/albertpumarola/D-NeRF) | [🌐 Project Page](https://www.albertpumarola.com/research/D-NeRF/index.html)  


### 2. [Arxiv '2023] Periodic Vibration Gaussian: Dynamic Urban Scene Reconstruction and Real-time Rendering
**Authors**: Yurui Chen, Chun Gu, Junzhe Jiang, Xiatian Zhu, Li Zhang
<details span>
<summary><b>Abstract</b></summary>
  Modeling dynamic, large-scale urban scenes is challenging due to their highly intricate geometric structures and unconstrained dynamics in both space and time. Prior methods often employ high-level architectural priors, separating static and dynamic elements, resulting in suboptimal capture of their synergistic interactions. To address this challenge, we present a unified representation model, called Periodic Vibration Gaussian (PVG). PVG builds upon the efficient 3D Gaussian splatting technique, originally designed for static scene representation, by introducing periodic vibration-based temporal dynamics. This innovation enables PVG to elegantly and uniformly represent the characteristics of various objects and elements in dynamic urban scenes. To enhance temporally coherent and large scene representation learning with sparse training data, we introduce a novel temporal smoothing mechanism and a position-aware adaptive control strategy respectively. Extensive experiments on Waymo Open Dataset and KITTI benchmarks demonstrate that PVG surpasses state-of-the-art alternatives in both reconstruction and novel view synthesis for both dynamic and static scenes. Notably, PVG achieves this without relying on manually labeled object bounding boxes or expensive optical flow estimation. Moreover, PVG exhibits 900-fold acceleration in rendering over the best alternative.
</details>

  [📄 Paper](https://arxiv.org/pdf/2311.18561) | [💻 Code](https://github.com/fudan-zvg/PVG) | [🌐 Project Page](https://fudan-zvg.github.io/PVG/)  

