---
title: "A Fast and Safe Motion Planning Algorithm in Cluttered Environment using Maximally Occupying Convex Space"
date: 2020-09-09 00:00:00 -0400
categories: research
---

<div style="font-size: 15px; line-height: 25px;">
This paper presents a new planning method in cluttered environment using a newly defined concept called a maximally occupying convex space (MOCS). Motion planning methods that use safe flight corridor (SFC) generally construct SFC in every new trial based on each initial path. We define a MOCS in a three-dimensional rectangular world to be prebuilt as SFC, prior to the initial path computation that leads to optimization process without running SFC construction phase. In the rectangular world, creating every possible MOCS covers all the free space overlapping with others if there exists a feasible path among those spaces. Thus, expressing MOCSs as nodes and their overlappings as edges, we can formulate a simplified graph representing the free space. Dijkstra algorithm is applied to a simplified graph in this work. This approach enables to omit constructing SFC every new trial, and to use path planning algorithm with small amount of nodes thereby, achieve efficient computation. We provide a completeness of a planning algorithm in a rectangular space, and show computation efficiency compared with a state-of-the-art algorithm based on SFC. <br>
<br>
 <center><a href="https://youtu.be/USFbCB9flEY" target="_blank">video</a></center>
</div>
