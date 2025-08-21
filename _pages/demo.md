---
title: "Demo"
layout: default
excerpt: "Demo"
sitemap: false
permalink: /demo/
---

# Demo


### [2] FQsun: A wave-function based emulator

We use FPGA ZCU102 to emulate a (up to 30 qubits) quantum system, based on state-vector (wave-function variant).

Scientific paper (ACCESS): [[link]](https://ieeexplore.ieee.org/document/11015479/) [[pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=11015479) [[code]](https://github.com/NAIST-Archlab/FQsun)


<p align="left">
    <img src="../images/paper/fqsun_arch.png" alt="FQsun Demo" style="max-width:60%; width:60%;">
</p>

*Figure 2.1. Overview architecture of our FQsun at the system-on-chip (Soc) level on FPGA. The arrow stands for dataflow. FQsun in PL communicates with PS through AXI Mapper and DMA Controller.*

<p align="left">
    <img src="../images/paper/fqsun_result.png" alt="ECG Demo" style="max-width:100%; width:100%;">
</p>

*Figure 2.2. The execution time comparison*

<!-- Check the [video demo](https://youtu.be/RAKSJXHCnf8?si=DLvXDAGBIEGdkT-t) for more information:

<iframe width="100%" height = "400px" src="https://www.youtube.com/embed/RAKSJXHCnf8?si=eaEJf4_6Dp-5yv0A" title="ECG demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe> -->






### [1] ECG processing for medical application

We propose a 1D-CNN accelerate (MINA) for processing ECG signal series for detecting heart disease. 

Scientific paper (TCAS-I): [[link]](https://ieeexplore.ieee.org/abstract/document/10948469/) [[pdf]](https://drive.google.com/file/d/1bXJ22whhtUEaHsR4Y5SIYyDlCiS9yMy4/view?usp=sharing) [[code]](https://github.com/AISeQLab/DEMO_MINA)

<p align="left">
    <img src="../images/paper/ecg_mina.png" alt="ECG Demo" style="max-width:60%; width:60%;">
</p>

*Figure 1.1. MINA overview architecture*

<p align="left">
    <img src="../images/paper/ecg_compare.png" alt="ECG Demo" style="max-width:100%; width:100%;">
</p>

*Figure 1.2. Comparison with fpga-based 2-d cnn hardware architectures for ecg classification.*

Check the [video demo](https://youtu.be/RAKSJXHCnf8?si=DLvXDAGBIEGdkT-t) for more information:

<iframe width="100%" height = "400px" src="https://www.youtube.com/embed/RAKSJXHCnf8?si=eaEJf4_6Dp-5yv0A" title="ECG demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
