# Awesome Articulated Objects Generation
## Table of contents

- [Generation](#generation)

## Generation

### 1. Sync4D: Video Guided Controllable Dynamics for Physics-Based 4D Generation
*Sync4D, arXiv 2024*

[📄 Paper](https://arxiv.org/abs/2405.16849) | [🌐 Project Page](https://sync4dphys.github.io/)
- Input: Prompt, RGB Video
<details span>
<summary><b>Abstract</b></summary>
<br>

In this work, we introduce a novel approach for creating controllable dynamics in 3D-generated Gaussians using casually captured reference videos. Our method transfers the motion of objects from reference videos to a variety of generated 3D Gaussians across different categories, ensuring precise and customizable motion transfer. We achieve this by employing blend skinning-based non-parametric shape reconstruction to extract the shape and motion of reference objects. This process involves segmenting the reference objects into motion-related parts based on skinning weights and establishing shape correspondences with generated target shapes. To address shape and temporal inconsistencies prevalent in existing methods, we integrate physical simulation, driving the target shapes with matched motion. This integration is optimized through a displacement loss to ensure reliable and genuine dynamics. Our approach supports diverse reference inputs, including humans, quadrupeds, and articulated objects, and can generate dynamics of arbitrary length, providing enhanced fidelity and applicability. Unlike methods heavily reliant on diffusion video generation models, our technique offers specific and high-quality motion transfer, maintaining both shape integrity and temporal consistency.
</details>

### 2. Puppet-Master: Scaling Interactive Video Generation as a Motion Prior for Part-Level Dynamics
*Puppet-Master, arXiv 2024*

[📄 Paper](https://arxiv.org/abs/2408.04631) | [🌐 Project Page](http://vgg-puppetmaster.github.io/)

- Dataset: Objaverse
- Input: Single RGB Image, motion trajectories
<details span>
<summary><b>Abstract</b></summary>
<br>

We present Puppet-Master, an interactive video generative model that can serve as a motion prior for part-level dynamics. At test time, given a single image and a sparse set of motion trajectories (i.e., drags), Puppet-Master can synthesize a video depicting realistic part-level motion faithful to the given drag interactions. This is achieved by fine-tuning a large-scale pre-trained video diffusion model, for which we propose a new conditioning architecture to inject the dragging control effectively. More importantly, we introduce the all-to-first attention mechanism, a drop-in replacement for the widely adopted spatial attention modules, which significantly improves generation quality by addressing the appearance and background issues in existing models. Unlike other motion-conditioned video generators that are trained on in-the-wild videos and mostly move an entire object, Puppet-Master is learned from Objaverse-Animation-HQ, a new dataset of curated part-level motion clips. We propose a strategy to automatically filter out sub-optimal animations and augment the synthetic renderings with meaningful motion trajectories. Puppet-Master generalizes well to real images across various categories and outperforms existing methods in a zero-shot manner on a real-world benchmark.
</details>

### 3. PhysPart: Physically Plausible Part Completion for Interactable Objects
*PhysPart, arXiv 2024*

[📄 Paper](https://www.arxiv.org/abs/2408.13724)
- Dataset: GAPartNet
- Input: Single Point Cloud
<details span>
<summary><b>Abstract</b></summary>
<br>
Interactable objects are ubiquitous in our daily lives. Recent advances in 3D generative models make it possible to automate the modeling of these objects, benefiting a range of applications from 3D printing to the creation of robot simulation environments. However, while significant progress has been made in modeling 3D shapes and appearances, modeling object physics, particularly for interactable objects, remains challenging due to the physical constraints imposed by inter-part motions. In this paper, we tackle the problem of physically plausible part completion for interactable objects, aiming to generate 3D parts that not only fit precisely into the object but also allow smooth part motions. To this end, we propose a diffusion-based part generation model that utilizes geometric conditioning through classifier-free guidance and formulates physical constraints as a set of stability and mobility losses to guide the sampling process. Additionally, we demonstrate the generation of dependent parts, paving the way toward sequential part generation for objects with complex part-whole hierarchies. Experimentally, we introduce a new metric for measuring physical plausibility based on motion success rates. Our model outperforms existing baselines over shape and physical metrics, especially those that do not adequately model physical constraints. We also demonstrate our applications in 3D printing, robot manipulation, and sequential part generation, showing our strength in realistic tasks with the demand for high physical plausibility.
</details>

### 4. NAP: Neural 3D Articulation Prior

*NAP, NIPS 2023*

[📄 Paper](https://arxiv.org/abs/2305.16315) | [🌐 Project Page](https://www.cis.upenn.edu/~leijh/projects/nap/) | [💻 Code](https://github.com/JiahuiLei/NAP)

<details span>
<summary><b>Abstract</b></summary>
<br>


We propose Neural 3D Articulation Prior (NAP), the first 3D deep generative model to synthesize 3D articulated object models. Despite the extensive research on generating 3D objects, compositions, or scenes, there remains a lack of focus on capturing the distribution of articulated objects, a common object category for human and robot interaction. To generate articulated objects, we first design a novel articulation tree/graph parameterization and then apply a diffusion-denoising probabilistic model over this representation where articulated objects can be generated via denoising from random complete graphs. In order to capture both the geometry and the motion structure whose distribution will affect each other, we design a graph-attention denoising network for learning the reverse diffusion process. We propose a novel distance that adapts widely used 3D generation metrics to our novel task to evaluate generation quality, and experiments demonstrate our high performance in articulated object generation. We also demonstrate several conditioned generation applications, including Part2Motion, PartNet-Imagination, Motion2Part, and GAPart2Object.
</details>

### 5. CAGE: Controllable Articulation Generation

*CAGE, arXiv 2023*

[📄 Paper](https://arxiv.org/abs/2312.09570) | [🌐 Project Page](https://3dlg-hcvc.github.io/cage/) | [💻 Code](https://github.com/3dlg-hcvc/cage)

- Dataset: PartNet-Mobility

<details span>
<summary><b>Abstract</b></summary>
<br>

We address the challenge of generating 3D articulated objects in a controllable fashion. Currently, modeling articulated 3D objects is either achieved through laborious manual authoring, or using methods from prior work that are hard to scale and control directly. We leverage the interplay between part shape, connectivity, and motion using a denoising diffusion-based method with attention modules designed to extract correlations between part attributes. Our method takes an object category label and a part connectivity graph as input and generates an object's geometry and motion parameters. The generated objects conform to user-specified constraints on the object category, part shape, and part articulation. Our experiments show that our method outperforms the state-of-the-art in articulated object generation, producing more realistic objects while conforming better to user constraints.
</details>

### 6. MeshArt: Generating Articulated Meshes with Structure-guided Transformers

*MeshArt, CVPR 2025*

[📄 Paper](https://arxiv.org/abs/2412.11596) | [🌐 Project Page](https://daoyig.github.io/Mesh_Art/)

- Dataset: PartNet

<details span>
<summary><b>Abstract</b></summary>
<br>

Articulated 3D object generation is fundamental for creating realistic, functional, and interactable virtual assets which are not simply static. We introduce MeshArt, a hierarchical transformer-based approach to generate articulated 3D meshes with clean, compact geometry, reminiscent of human-crafted 3D models. We approach articulated mesh generation in a part-by-part fashion across two stages. First, we generate a high-level articulation-aware object structure; then, based on this structural information, we synthesize each part's mesh faces. Key to our approach is modeling both articulation structures and part meshes as sequences of quantized triangle embeddings, leading to a unified hierarchical framework with transformers for autoregressive generation. Object part structures are first generated as their bounding primitives and articulation modes; a second transformer, guided by these articulation structures, then generates each part's mesh triangles. To ensure coherency among generated parts, we introduce structure-guided conditioning that also incorporates local part mesh connectivity. MeshArt shows significant improvements over state of the art, with 57.1% improvement in structure coverage and a 209-point improvement in mesh generation FID.
</details>

### 7. SINGAPO: Single Image Controlled Generation of Articulated Parts in Object

*SINGAPO, arXiv 2024*

[📄 Paper](https://arxiv.org/abs/2410.16499) | [🌐 Project Page](https://3dlg-hcvc.github.io/singapo/) | [💻 Code](https://github.com/3dlg-hcvc/singapo)

- Level: Category-Level
- Dataset: PartNet-Mobility
- Input: Single RGB Image
<details span>
<summary><b>Abstract</b></summary>
<br>
We address the challenge of creating 3D assets for household articulated objects from a single image. Prior work on articulated object creation either requires multi-view multi-state input, or only allows coarse control over the generation process. These limitations hinder the scalability and practicality for articulated object modeling. In this work, we propose a method to generate articulated objects from a single image. Observing the object in resting state from an arbitrary view, our method generates an articulated object that is visually consistent with the input image. To capture the ambiguity in part shape and motion posed by a single view of the object, we design a diffusion model that learns the plausible variations of objects in terms of geometry and kinematics. To tackle the complexity of generating structured data with attributes in multiple domains, we design a pipeline that produces articulated objects from high-level structure to geometric details in a coarse-to-fine manner, where we use a part connectivity graph and part abstraction as proxies. Our experiments show that our method outperforms the state-of-the-art in articulated object creation by a large margin in terms of the generated object realism, resemblance to the input image, and reconstruction quality.
</details>

### 8. ArtiLatent: Realistic Articulated 3D Object Generation via Structured Latents

**stay tuned**

### 9.PhysX-3D: Physical-Grounded 3D Asset Generation

**stay tuned**[CVPR 2026](https://cvpr.thecvf.com/Conferences/2026)

### 10.PhysX-Anything: Simulation-Ready Physical 3D Assets from Single Image

**stay tuned**[NeurIPS 2025 (Spotlight)](https://neurips.cc/)

### 11. ArtLLM: Generating Articulated Assets via 3D LLM

**stay tuned[CVPR 2026](https://cvpr.thecvf.com/Conferences/2026)**

### 12. PAct: Part-Decomposed Single-View Articulated Object Generation

**stay tuned ** Part-center **latest SOTA**

Liu Q, Yao X, Zhang S, et al. PAct: Part-Decomposed Single-View Articulated Object Generation[J]. arXiv preprint arXiv:2602.14965, 2026.










