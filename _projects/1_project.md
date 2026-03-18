---
layout: page
title: Novel View Pose Synthesis with Geometry-Aware Regularization for Enhanced 3D Gaussian Splatting
description: POSTECH Computer Graphics Lab
img: assets/img/cg.png
importance: 1
category: 2025
---

## Project Goal

- Enhance the quality of 3D reconstruction  
- Improve multi-view consistency  
- Incorporate geometry-aware loss terms for accurate surface reconstruction  

<br>
<br>

## Project Page

----------

<div style="text-align: center;">
    <iframe src="https://chehun16.github.io/gs-quality/" width="800" height="400" 
            style="display: block; margin: auto; border: none;"></iframe>
</div>


<p style="color: gray; font-size: 0.8em;">
    Detailed information about the project can be found in the 
    <a href="https://chehun16.github.io/gs-quality/" target="_blank" style="color: gray; text-decoration: underline;">
        project page
    </a> above!
</p>

<ul>
  <li><a href="https://chehun16.github.io/gs-quality/" target="_blank">Project page</a></li>
  <li><a href="https://lacy-tick-ae2.notion.site/Novel-View-Pose-Synthesis-with-Geometry-Aware-Regularization-for-Enhanced-3D-Gaussian-Splatting-245b0c1a844f80e096fbd720f5484f0d" target="_blank">Project detail</a></li>
</ul>

---------------

<br>
<br>

## Project Overview

<p align="center">
  <img src="./assets/img/pipeline1.png" width="600">
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="./assets/img/pipeline2.png" width="600">
</p>

I developed a method to enhance indoor 3D reconstruction with **3D Gaussian Splatting (3DGS)** by generating  
novel view camera poses, refining them with **DIFIX**, and applying **geometry-aware loss terms**.  
This approach improves geometry accuracy, multi-view consistency, and reduces artifacts.

<br>
<br>

## Contributions

1. **Novel view camera pose generation**
   - Expanded spatial coverage and ensured consistency between viewpoints  
   - Removed artifacts in novel-view renderings using **DIFIX**

2. **Introduction of additional loss terms**
   - Applied **LPIPS loss** only to novel views to preserve structural details beyond pixel similarity  
   - Applied **normal consistency loss** and **depth smoothness loss** to all views to improve geometry quality  

<br>
<br>

## Results


<table style="margin-left:auto; margin-right:auto; border-collapse: collapse; text-align: center;">
  <thead>
    <tr>
      <th>Method</th>
      <th>Initial Points</th>
      <th>PSNR ↑</th>
      <th>SSIM ↑</th>
      <th>Training Time</th>
      <th>Frames</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3DGS</td>
      <td>100,000</td>
      <td>20.423</td>
      <td>0.856</td>
      <td>2h 13m</td>
      <td>168</td>
    </tr>
    <tr>
      <td>2DGS</td>
      <td>100,000</td>
      <td>19.219</td>
      <td>0.828</td>
      <td>2h 1m</td>
      <td>168</td>
    </tr>
    <tr>
      <td>2DGS (Novel)</td>
      <td>100,000</td>
      <td>20.375</td>
      <td>0.842</td>
      <td>1h 59m</td>
      <td>208</td>
    </tr>
    <tr>
      <td><strong>Ours (Novel)</strong></td>
      <td>100,000</td>
      <td><strong>21.605</strong></td>
      <td><strong>0.861</strong></td>
      <td>2h 6m</td>
      <td>208</td>
    </tr>
    <tr>
      <td style="color: indianred; font-weight: bold;">Ours + Loss</td>
      <td>100,000</td>
      <td style="color: indianred; font-weight: bold;">21.675</td>
      <td style="color: indianred; font-weight: bold;">0.862</td>
      <td>3h 55m</td>
      <td>208</td>
    </tr>
  </tbody>
</table>


<br>

- Compared to **3DGS**, our method improves **PSNR from 20.423 → 21.675** and **SSIM from 0.856 → 0.862**  
- Applying the method to **2DGS** also yields consistent improvements, demonstrating generalizability  


<br>
<br>

## Visualization

<p align="center">
  <video width="320" controls>
    <source src="assets/video/cg1.mp4" type="video/mp4">
  </video>
  <video width="320" controls>
    <source src="assets/video/cg2.mp4" type="video/mp4">
  </video>
</p>


<br>

<div style="border: 1.5px solid var(--global-theme-color); background-color: transparent; padding: 15px; margin-top: 20px; border-radius: 5px; font-size: 14px;">
    <strong>🧑‍💻 My Role:</strong> Conceived the research idea, designed the methodology, and carried out the entire implementation 
    — including dataset preparation, novel view generation, loss function integration, and experimental evaluation — with advisory 
    input from a doctoral researcher.
</div>

<br>
<br>
<br>

<a href="https://github.com/chehun16/3dgs-quality" style="text-decoration: none; display: inline-flex; align-items: center; padding: 6px 10px; background-color: #333; color: white; border-radius: 5px; font-size: 14px; font-weight: bold;">
    <img src="https://github.com/fluidicon.png" alt="GitHub" style="width: 18px; height: 18px; margin-right: 5px; filter: invert(1);">
    3dgs-quality-enhancement
</a>