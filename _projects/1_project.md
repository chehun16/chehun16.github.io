---
layout: page
title: Novel View Pose Synthesis with Geometry-Aware Regularization for Enhanced 3D Gaussian Splatting
description: POSTECH Computer Graphics Lab
img: assets/img/cg.png
importance: 1
category: work
---

@POSTECH Computer Graphics Lab

<h2>Project Goal</h2>
<ul>
    <li>Enhance the quality of 3D reconstruction</li>
    <li>Improve multi view consistency</li>
    <li>Incorporate geometry-aware loss terms for accurate surface reconstruction</li>
</ul>

<h2>Project Page</h2>

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

<br>

<h2>Project Overview</h2>

<p align="center">
    <img src="/images/pipeline1.png" alt="cg" width="600">
</p>
<p align="center">⇣</p>
<p align="center">
    <img src="/images/pipeline2.png" alt="cg" width="600">
</p>

<p>
I developed a method to enhance indoor 3D reconstruction with 3D Gaussian Splatting (3DGS) by generating 
novel view camera poses, refining them with DIFIX, and applying geometry-aware loss terms. This approach 
improved geometry accuracy, multi-view consistency, and reduced artifacts.
</p>

<br>

<h2>Contributions</h2>
<ol>
  <li>
    Novel view camera pose generation
    <ul>
      <li>Expanded spatial coverage and ensured consistency between viewpoints.</li>
      <li>Removed artifacts in scenes rendered from novel view camera poses using DIFIX.</li>
    </ul>
  </li>
  <li>
    Introduction of additional loss terms
    <ul>
      <li>Added a perceptual LPIPS loss applied only to novel views to preserve not only pixel information but also structural details.</li>
      <li>Applied normal consistency loss and depth smoothness loss to all views to improve geometry reconstruction quality.</li>
    </ul>
  </li>
</ol>


<br>

<h2>Results</h2>
<table border="1" cellspacing="0" cellpadding="6" style="border-collapse: collapse; text-align: center; margin: auto;">
  <thead>
    <tr>
      <th>method</th>
      <th>initial point#</th>
      <th>PSNR↑</th>
      <th>SSIM↑</th>
      <th>Training time</th>
      <th>frame#</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3DGS</td>
      <td>100000</td>
      <td>20.423</td>
      <td>0.856</td>
      <td>2h 13m</td>
      <td>168</td>
    </tr>
    <tr>
      <td>2DGS</td>
      <td>100000</td>
      <td>19.219</td>
      <td>0.828</td>
      <td>2h 1m</td>
      <td>168</td>
    </tr>
    <tr>
      <td>2DGS_novel</td>
      <td>100000</td>
      <td>20.375</td>
      <td>0.842</td>
      <td>1h 59m</td>
      <td>208</td>
    </tr>
    <tr>
      <td>Ours_novel</td>
      <td>100000</td>
      <td style="color: rgb(105, 126, 204);">21.605</td>
      <td style="color: rgb(105, 126, 204);">0.861</td>
      <td>2h 6m</td>
      <td>208</td>
    </tr>
    <tr>
      <td style="color: indianred;">Ours_novel_loss</td>
      <td>100000</td>
      <td style="color: indianred;">21.675</td>
      <td style="color: indianred;">0.862</td>
      <td>3h 55m</td>
      <td>208</td>
    </tr>
  </tbody>
</table>

<br>
<ul>
  <li>Compared to 3DGS, our method achieved a <strong>PSNR</strong> improvement from 20.423 to <strong>21.675</strong> and an <strong>SSIM</strong> increase from 0.856 to <strong>0.862</strong>.</li>
  <li>Applying our method to 2DGS also yielded higher scores, demonstrating its generalizability.</li>
</ul>

<br>


<div style="display: flex; justify-content: center; gap: 20px;">
    <video width="320" controls>
        <source src="/videos/cg1.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>

    <video width="320" controls>
        <source src="/videos/cg2.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
</div>

<br>

<div style="border-left: 6px solid #007BFF; background-color: #f0f8ff; padding: 15px; margin-top: 20px; border-radius: 5px; font-size: 14px;">
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