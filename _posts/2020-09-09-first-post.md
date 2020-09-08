---
title: "A novel computationally efficient method to return safe trajectories"
date: 2020-09-09 00:00:00 -0400
categories: research
---
<center><strong> A Fast and Safe Motion Planning Algorithm in Cluttered Environment using Maximally Occupying Convex Space</strong> <br>
  Youngsang Suh, Jiseock Kang, Dongjun Lee <br>
  ICCAS 2020 <br> </center>

<div style="font-size: 15px; line-height: 25px;">
This work presents a new planning method in cluttered environment using a newly defined concept called maximally occupying convex space (MOCS). Motion planning methods that use safe flight corridor (SFC) generally construct SFC in every new trial based on each initial path. We define MOCS in three-dimensional rectangular world to be prebuilt as SFC prior to the initial path computation. This approach enables to omit constructing SFC every new trial, and our experiment shows computation efficiency compared to a state-of-the-art algorithm based on SFC. <br>
 
 <center><a href="https://youtu.be/USFbCB9flEY" target="_blank">video</a></center>
</div>

<hr class="one">
<strong> Background </strong><br>

<div style="font-size: 15px; line-height: 25px;">
<strong>SFC? </strong> <br>

SFC consists of overlapping convex spaces that guarantee collision avoidance when waypoints are located inside the overlapping areas. Through utilizing SFC, the system can return safe trajectories owing to the property of SFC. <br>

<center><img src="/assets/images/SFC.png" border="0" width="360" height="330"/> </center> <br>
</div>

<hr class="one">
<strong> Motivation </strong> <br>

<div style="font-size: 15px; line-height: 25px;"> 
Fast and safe motion planning of UAV is still a crucial task to achieve. However, previous studies that utilize SFC need seed points or initial paths to construct SFC. If we generate every possible SFC in the free space priori, the system can have computational efficiency to return safe trajectories. It is because SFC does not have to be constructed every trial, which reduces computation time. <br>
</div>

<hr class="one">
<strong> Task </strong> <br>

<div style="font-size: 15px; line-height: 25px;">
To prebuild every possible SFC, we have to define a convex space and prove that those spaces represent every feasible path in the free space. After the proof, an algorithm that generates every defined convex space should be devised. <br>

</div>

<hr class="one">
<strong> Approach </strong> <br>
 
<div style="font-size: 15px; line-height: 25px;">
How should we define a specific convex space to fill the whole free space without seed points? <br>
Our approach is to use inclusion relation with other convex spaces. With this approach, one can simply (1) make locally maximum convex spaces and (2) use mathematical knowledge to prove the equivalence between feasible paths.

<br>
Furthermore, we use dynamic programming method to construct an algorithm. Dynamic programming is a powerful technique because almost all of the algorithms can be made by this method. <br>
</div>
