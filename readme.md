# awesome-4D-reconstruction

A curated list of papers and open-source resources focused on 4D reconstruction model. 

### 1. [CVPR '2021] D-NeRF: Neural Radiance Fields for Dynamic Scenes
**Authors**: Albert Pumarola, Enric Corona, Gerard Pons-Moll, Francesc Moreno-Noguer
<details span>
<summary><b>Abstract</b></summary>
  Neural rendering techniques combining machine learning with geometric reasoning have arisen as one of the most promising approaches for synthesizing novel views of a scene from a sparse set of images. Among these, stands out the Neural radiance fields (NeRF), which trains a deep network to map 5D input coordinates (representing spatial location and viewing direction) into a volume density and view-dependent emitted radiance. However, despite achieving an unprecedented level of photorealism on the generated images, NeRF is only applicable to static scenes, where the same spatial location can be queried from different images. In this paper we introduce D-NeRF, a method that extends neural radiance fields to a dynamic domain, allowing to reconstruct and render novel images of objects under rigid and non-rigid motions from a \emph{single} camera moving around the scene. For this purpose we consider time as an additional input to the system, and split the learning process in two main stages: one that encodes the scene into a canonical space and another that maps this canonical representation into the deformed scene at a particular time. Both mappings are simultaneously learned using fully-connected networks. Once the networks are trained, D-NeRF can render novel images, controlling both the camera view and the time variable, and thus, the object movement. We demonstrate the effectiveness of our approach on scenes with objects under rigid, articulated and non-rigid motions.
</details>

  [📄 Paper](https://arxiv.org/pdf/2011.13961) | [💻 Code](https://github.com/albertpumarola/D-NeRF) | [🌐 Project Page](https://www.albertpumarola.com/research/D-NeRF/index.html)  


