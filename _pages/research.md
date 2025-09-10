---
title: "Research"
layout: default
excerpt: "Research"
sitemap: false
permalink: /research/
---
# Tutorials

[High-bandwidth memory usage](https://github.com/AISeQLab/HBM_Tutorial/blob/main/HBM_Tutorial_Markdown/HIGH%20BANDWIDTH%20MEMORY%20(HBM)%202548ba96de7f8077bdb9ccb8f0f1ab4f.md)


# AI Projects

Currently blank.

# Se Projects

There are projects for Gen 1, calling from Facebook group.

[List of existing projects](https://docs.google.com/spreadsheets/d/1gswsvpBxHxGYJV5gXpZ4qD-7IA735JHvY7n1P2ABLPI/edit?usp=sharing)

[List of members](https://docs.google.com/spreadsheets/d/1vrbcvRWvCJI2dvyBgF6bYcGPCktQ7GpC1CKx0sXq1OQ/edit?usp=sharing)

# Q Projects
### Emulating the decision diagram
**Project Type:** Big project  
**Introduction:** Quantum simulation has been identified as a difficult computational problem with resources exponentially increasing based on the number of qubits. The basic representation of a quantum system is a state-vector, which for any $n$ qubits requires processing a $2^{n}$ complex array. A more efficient way to deal with this problem is to change the representation using a decision diagram. This approach saves on redundant computations by acting on a compact representation instead of the full-state vector.  
**Inputs:** The initial state $$|0\rangle^{\otimes n}$$ and a list of quantum unitary operators $$\{U_{j}\}$$.  
**Output:** The final state $|\psi\rangle=U_{m}U_{m-1}...U_{0}|0\rangle^{\otimes n}$.  
**Target:** To emulate the system described in reference [3] on an FPGA to make it faster than the original C++ version.  



---

### Matrix-product state
**Project Type:** Big project  
**Introduction:** Quantum simulators have exponential complexity $(\mathcal{O}(2^{n}))$ in both time and space aspects for simulation on a classical computer. This can be reduced to a polynomial complexity by using the matrix product state (MPS) method, which efficiently processes low-entanglement states. Any state $|\psi\rangle$ can be written as an MPS via Singular-Value-Decomposition (SVD). SVD decomposes any matrix $M$ as $M=U\Lambda V^{\dagger}$, where $\Lambda$ is a diagonal matrix of non-negative singular values, and $U$ and $V^{\dagger}$ are left and right-unitary matrices.  
**Gate Application:** A quantum gate applied to an MPS can be either a local or a non-local gate. Local gates, such as single-qubit gates or neighboring n-qubit gates, can be applied directly. Non-local gates are more complicated and require the qubits to be swapped, applied, and then re-swapped.  
**Inputs:** The initial state $|0\rangle^{\otimes n}$ and a list of quantum unitary operators $\{U_{j}\}$.  
**Output:** The final state $|\psi\rangle=U_{m}U_{m-1}...U_{0}|0\rangle^{\otimes n}$.  
**Target:** The main operations in MPS are the SVD operation (conducted n times for n qubits) and non-local/local gate application (which is simply matrix multiplication). While SVD and matrix multiplication have been accelerated on many types of hardware, there is no current proposal for accelerating both in a unified hardware.  

---

### Linear combination of unitaries
**Project Type:** Small project  
**Introduction:** Any hermitian can be decomposed into a linear combination of unitaries: $H=\Sigma\alpha_{j}U_{j}$. The coefficients $\{\alpha_{j}\}$ are complex, and the unitaries $\{U_{j}\}$ are constructed from the Pauli basis {I, X, Y, Z}. The most effective way to get $\{\alpha_{j},U_{j}\}$ is to use the Walsh-Hadamard transform. The classical version of this process has a time complexity of $\mathcal{O}(n4^{n})$, which quickly becomes overloaded for $n>10$.  
**Inputs:** An initial hermitian matrix $H$.  
**Output:** $\{\alpha_{j},U_{j}\}$.  
**Target:** To apply acceleration techniques to solve the equation. It is noted that $H$ satisfies $HH^{T}=I$ and all $U_{j}$ follow certain rules.  

---

### Accelerating Lanczos algorithm
**Project Type:** Small project  
**Introduction:** The Lanczos algorithm helps to find the $k$ smallest or biggest eigenvalues on an extremely large hermitian matrix $L$ by distilling $L\in\mathbb{R}^{N\times N}$ to a smaller matrix $T\in\mathbb{R}^{k\times k}$ where $k\ll N$. Finding the $k$ eigenvalues on $T$ can then be done in $O(k^{3})$ instead of $\mathcal{O}(N^{3})$. The complexity of the Lanczos algorithm, $\mathcal{O}(kN^{2})$, comes from $k$ iterations of matrix-vector multiplication $Lv_{i}$.  
**Inputs:** A hermitian matrix $L$.  
**Output:** The matrix $T$.  
**Target:** To reduce the complexity from $\mathcal{O}(kN^{2})$ to $\mathcal{O}(k^{\prime}N^{2})$ with $k^{\prime}\ll k$ on an FPGA.  
