---
title: "Developing a Model for Improving 3D Gaussian Splatting Performance Based on DBSCAN"
collection: publications
category: manuscripts
permalink: /publication/2024-11-01-gaussian-dbscan
excerpt: 'This paper presents a model to enhance 3D Gaussian Splatting performance using DBSCAN clustering.'
date: 'Nov, 2024'
venue: 'IEIE 2024'
slidesurl: 'https://deep-daiv-computer-vision.github.io/3DGS_DIET/'
paperurl: '/files/paper1.pdf'
citation: 'Dayeon Woo<sup>‡1</sup>, Eunseo Seo<sup>‡2</sup>, Chehun Han<sup>‡3</sup>, Yeonkyung Lee<sup>‡4</sup>, *Changgyun Jin<sup>5</sup> (‡: Equally Contributed)'
---

This paper proposes a model that improves the performance of **3D Gaussian Splatting (3DGS)** while reducing memory usage. The model utilizes **DBSCAN clustering** to optimize Gaussian representations, leading to more efficient and accurate 3D rendering.

<br>

<iframe src="/files/paper1.pdf#toolbar=0&navpanes=0&scrollbar=0" width="800" height="400" style="display: block; margin: auto; border: none;"></iframe>

<br>

|  | SSIM | PSNR | Mem | num |
| --- | --- | --- | --- | --- |
| M-NeRF360 | 0.759 | 22.22 | 8.6MB | - |
| 3DGS | 0.841 | 23.14 | 411MB | 1.78 |
| Ours-1 | **<span style="color: IndianRed;">0.887</span>** | **<span style="color: IndianRed;">25.57</span>** | 387.6MB | 1.63 |
| Ours-3 | 0.885 | 25.21 | **<span style="color: IndianRed;">384.4MB</span>** | **<span style="color: IndianRed;">1.62</span>** |

The evaluation metrics for image quality, **SSIM** and **PSNR**, show that **<span style="color: IndianRed;">Ours-1</span>** (DBSCAN applied once) and **<span style="color: IndianRed;">Ours-3</span>** (DBSCAN applied three times) achieved **<span style="color: IndianRed;">higher similarity</span>** than 3DGS.

Additionally, **<span style="color: IndianRed;">memory usage was reduced by approximately 10%</span>** in both Ours-1 and Ours-3 compared to 3DGS.

<br>

<a href="https://github.com/chehun16/autonomous-engine" style="text-decoration: none; display: inline-flex; align-items: center; padding: 6px 10px; background-color: #333; color: white; border-radius: 5px; font-size: 14px; font-weight: bold;">
    <img src="https://github.com/fluidicon.png" alt="GitHub" style="width: 18px; height: 18px; margin-right: 5px; filter: invert(1);">
    3DGS_Diet
</a>