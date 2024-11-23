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


### 3. [CVPR '2024] DrivingGaussian: Composite Gaussian Splatting for Surrounding Dynamic Autonomous Driving Scenes
**Authors**: Xiaoyu Zhou, Zhiwei Lin, Xiaojun Shan, Yongtao Wang, Deqing Sun, Ming-Hsuan Yang
<details span>
<summary><b>Abstract</b></summary>
  We present DrivingGaussian, an efficient and effective framework for surrounding dynamic autonomous driving scenes. For complex scenes with moving objects, we first sequentially and progressively model the static background of the entire scene with incremental static 3D Gaussians. We then leverage a composite dynamic Gaussian graph to handle multiple moving objects, individually reconstructing each object and restoring their accurate positions and occlusion relationships within the scene. We further use a LiDAR prior for Gaussian Splatting to reconstruct scenes with greater details and maintain panoramic consistency. DrivingGaussian outperforms existing methods in dynamic driving scene reconstruction and enables photorealistic surround-view synthesis with high-fidelity and multi-camera consistency.
</details>

  [📄 Paper](https://arxiv.org/abs/2312.07920) | [💻 Code](https://github.com/VDIGPKU/DrivingGaussian) | [🌐 Project Page](https://pkuvdig.github.io/DrivingGaussian/)  


### 4. [ECCV '2024] Street Gaussians: Modeling Dynamic Urban Scenes with Gaussian Splatting
**Authors**: Yunzhi Yan, Haotong Lin, Chenxu Zhou, Weijie Wang, Haiyang Sun, Kun Zhan, Xianpeng Lang, Xiaowei Zhou, Sida Peng
<details span>
<summary><b>Abstract</b></summary>
  This paper aims to tackle the problem of modeling dynamic urban streets for autonomous driving scenes. Recent methods extend NeRF by incorporating tracked vehicle poses to animate vehicles, enabling photo-realistic view synthesis of dynamic urban street scenes. However, significant limitations are their slow training and rendering speed. We introduce Street Gaussians, a new explicit scene representation that tackles these limitations. Specifically, the dynamic urban scene is represented as a set of point clouds equipped with semantic logits and 3D Gaussians, each associated with either a foreground vehicle or the background. To model the dynamics of foreground object vehicles, each object point cloud is optimized with optimizable tracked poses, along with a 4D spherical harmonics model for the dynamic appearance. The explicit representation allows easy composition of object vehicles and background, which in turn allows for scene editing operations and rendering at 135 FPS (1066 × 1600 resolution) within half an hour of training. The proposed method is evaluated on multiple challenging benchmarks, including KITTI and Waymo Open datasets. Experiments show that the proposed method consistently outperforms state-of-the-art methods across all datasets.
</details>

  [📄 Paper](https://arxiv.org/pdf/2401.01339) | [💻 Code](https://github.com/zju3dv/street_gaussians) | [🌐 Project Page](https://zju3dv.github.io/street_gaussians/)  



### 5. [Arxiv '2024] MonST3R: A Simple Approach for Estimating Geometry in the Presence of Motion
**Authors**: Junyi Zhang, Charles Herrmann, Junhwa Hur, Varun Jampani, Trevor Darrell, Forrester Cole, Deqing Sun, Ming-Hsuan Yang
<details span>
<summary><b>Abstract</b></summary>
  Estimating geometry from dynamic scenes, where objects move and deform over time, remains a core challenge in computer vision. Current approaches often rely on multi-stage pipelines or global optimizations that decompose the problem into subtasks, like depth and flow, leading to complex systems prone to errors. In this paper, we present Motion DUSt3R (MonST3R), a novel geometry-first approach that directly estimates per-timestep geometry from dynamic scenes. Our key insight is that by simply estimating a pointmap for each timestep, we can effectively adapt DUST3R's representation, previously only used for static scenes, to dynamic scenes. However, this approach presents a significant challenge: the scarcity of suitable training data, namely dynamic, posed videos with depth labels. Despite this, we show that by posing the problem as a fine-tuning task, identifying several suitable datasets, and strategically training the model on this limited data, we can surprisingly enable the model to handle dynamics, even without an explicit motion representation. Based on this, we introduce new optimizations for several downstream video-specific tasks and demonstrate strong performance on video depth and camera pose estimation, outperforming prior work in terms of robustness and efficiency. Moreover, MonST3R shows promising results for primarily feed-forward 4D reconstruction.
</details>

  [📄 Paper](https://arxiv.org/pdf/2410.03825) | [💻 Code](https://github.com/Junyi42/monst3r) | [🌐 Project Page](https://monst3r-project.github.io/)  


### 6. [CVPR '2024] HUGS: Holistic Urban 3D Scene Understanding via Gaussian Splatting
**Authors**: Hongyu Zhou, Jiahao Shao, Lu Xu, Dongfeng Bai, Weichao Qiu, Bingbing Liu, Yue Wang, Andreas Geiger, Yiyi Liao
<details span>
<summary><b>Abstract</b></summary>
  Holistic understanding of urban scenes based on RGB images is a challenging yet important problem. It encompasses understanding both the geometry and appearance to enable novel view synthesis, parsing semantic labels, and tracking moving objects. Despite considerable progress, existing approaches often focus on specific aspects of this task and require additional inputs such as LiDAR scans or manually annotated 3D bounding boxes. In this paper, we introduce a novel pipeline that utilizes 3D Gaussian Splatting for holistic urban scene understanding. Our main idea involves the joint optimization of geometry, appearance, semantics, and motion using a combination of static and dynamic 3D Gaussians, where moving object poses are regularized via physical constraints. Our approach offers the ability to render new viewpoints in real-time, yielding 2D and 3D semantic information with high accuracy, and reconstruct dynamic scenes, even in scenarios where 3D bounding box detection are highly noisy. Experimental results on KITTI, KITTI-360, and Virtual KITTI 2 demonstrate the effectiveness of our approach.
</details>

  [📄 Paper](https://arxiv.org/pdf/2403.12722) | [💻 Code](https://github.com/hyzhou404/HUGS) | [🌐 Project Page](https://xdimlab.github.io/hugs_website/)  


### 7. [Arxiv '2024]OmniRe: Omni Urban Scene Reconstruction
**Authors**: Ziyu Chen, Jiawei Yang, Jiahui Huang, Riccardo de Lutio, Janick Martinez Esturo, Boris Ivanovic, Or Litany, Zan Gojcic, Sanja Fidler, Marco Pavone, Li Song, Yue Wang
<details span>
<summary><b>Abstract</b></summary>
  We introduce OmniRe, a holistic approach for efficiently reconstructing high-fidelity dynamic urban scenes from on-device logs. Recent methods for modeling driving sequences using neural radiance fields or Gaussian Splatting have demonstrated the potential of reconstructing challenging dynamic scenes, but often overlook pedestrians and other non-vehicle dynamic actors, hindering a complete pipeline for dynamic urban scene reconstruction. To that end, we propose a comprehensive 3DGS framework for driving scenes, named OmniRe, that allows for accurate, full-length reconstruction of diverse dynamic objects in a driving log. OmniRe builds dynamic neural scene graphs based on Gaussian representations and constructs multiple local canonical spaces that model various dynamic actors, including vehicles, pedestrians, and cyclists, among many others. This capability is unmatched by existing methods. OmniRe allows us to holistically reconstruct different objects present in the scene, subsequently enabling the simulation of reconstructed scenarios with all actors participating in real-time (~60Hz). Extensive evaluations on the Waymo dataset show that our approach outperforms prior state-of-the-art methods quantitatively and qualitatively by a large margin. We believe our work fills a critical gap in driving reconstruction.
</details>

  [📄 Paper](https://export.arxiv.org/pdf/2408.16760) | [💻 Code](https://github.com/ziyc/drivestudio) | [🌐 Project Page](https://ziyc.github.io/omnire/)  



