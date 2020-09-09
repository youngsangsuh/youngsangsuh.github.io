---
title: "A novel computationally efficient method to return safe trajectories"
date: 2020-09-09 00:00:00 -0400
categories: research
---

<div style="font-size: medium; line-height: 2em;">
<center><strong> A Fast and Safe Motion Planning Algorithm in Cluttered Environment using Maximally Occupying Convex Space</strong> <br>
  Youngsang Suh, Jiseock Kang, Dongjun Lee <br>
  ICCAS 2020 <br>
  <a href="/assets/pdf/A fast and safe motion planning algorithm in cluttered environment using maximally occupying convex space.pdf" target="_blank">paper</a> <a href="https://youtu.be/USFbCB9flEY" target="_blank">video</a> <br> </center>
</div>

<div style="font-size: 15px; line-height: 25px;">
<br>
This work presents a new planning method in cluttered environment using a newly defined concept called maximally occupying convex space (MOCS). Motion planning methods that use safe flight corridor (SFC) generally construct SFC in every new trial based on each initial path. We define MOCS in three-dimensional rectangular world to be prebuilt as SFC prior to the initial path computation. This approach enables to omit constructing SFC every new trial, and our experiment shows computation efficiency compared to a state-of-the-art algorithm based on SFC. <br>
 
</div>

<hr class="one">
<strong> Background </strong><br>

<div style="font-size: 15px; line-height: 25px;">
<strong>SFC? </strong> <br>

SFC consists of overlapping convex spaces that guarantee collision avoidance when waypoints are located inside the overlapping areas. Through utilizing SFC, the system can return safe trajectories owing to the property of SFC. <br><br>

<center><img src="/assets/images/SFC_.png" border="0" width="300" height="330"/> </center> <br>
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
How should we define a specific convex space to fill the whole free space without seed points? <br> <br>
Our approach is to use inclusion relation with other convex spaces. With this approach, one can simply (1) make locally maximum convex spaces and (2) use mathematical knowledge to prove the equivalence between feasible paths.

<br>
Furthermore, we use dynamic programming method to construct the algorithm. Dynamic programming is a powerful technique because almost all of the algorithms can be made by this method. <br>
</div>

<hr class="one">
<strong> Maximally Occupying Convex Space </strong> <br>

<div style="font-size: 15px; line-height: 25px;">
<strong>MOCS definition </strong> <br>
Given a rectangular world free space <img src="http://latex.codecogs.com/svg.latex?\mathbb{W}"/>, a set <img src="http://latex.codecogs.com/svg.latex?\mathbb{C}"/> of convex subsets in <img src="http://latex.codecogs.com/svg.latex?\mathbb{W}"/> and a set <img src="http://latex.codecogs.com/svg.latex?\mathbb{O}"/> of cuboid obstacles, a cuboid convex closed set <img src="http://latex.codecogs.com/svg.latex?C"/> is a maximally occupying convex space if and only if <img src="http://latex.codecogs.com/svg.latex?~\forall c \in"/> <img src="http://latex.codecogs.com/svg.latex?\mathbb{C}"/> s.t. <img src="http://latex.codecogs.com/svg.latex?c \not\subset C"/>, <img src="http://latex.codecogs.com/svg.latex?c \cup C"/> is not convex set. <br><br>

<center><img src="/assets/images/MOCS example.jpg" border="0" width="430" height="330"/> </center> <br>
Left: green convex space is not a MOCS, due to its union with red rectangle is a convex space. Right: green, light blue, purple convex spaces are MOCS that contain a blue point. <br><br>

<strong>Lemma </strong> <br>
For <img src="http://latex.codecogs.com/svg.latex?x \in"/> <img src="http://latex.codecogs.com/svg.latex?\text{int}(\mathbb{W})"/>, convex set <img src="http://latex.codecogs.com/svg.latex?S \subset \mathbb{W}"/>, let us define <img src="http://latex.codecogs.com/svg.latex?d_S(x) = min \{\| x-y \| ~|~ y \in \partial S \}"/>, <img src="http://latex.codecogs.com/svg.latex?D(x) = max\{ d_C(x) ~|~ x \in"/> <img src="http://latex.codecogs.com/svg.latex?\text{int}(C), ~ C \in M \}"/>. Then, <img src="http://latex.codecogs.com/svg.latex?D(x) > 0"/>. <br>

<strong>Theorem </strong> <br>
Please refer to our paper for further details and proofs.
  </div>
  
<hr class="one">
<strong> Algorithmic Implementation </strong> <br>
