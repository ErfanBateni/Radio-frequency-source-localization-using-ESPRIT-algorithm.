# Direction of Arrival (DOA) Estimation using ESPRIT Algorithm

This repository contains the course project for **Signals and Systems** at Sharif University of Technology. The project focuses on the theoretical analysis and practical implementation of the **ESPRIT** (Estimation of Signal Parameters via Rotational Invariance Techniques) algorithm for estimating the Direction of Arrival (DOA) of narrowband signals.

## 📌 Project Overview
The ESPRIT algorithm is a powerful, high-resolution subspace-based method used in signal processing and antenna arrays to detect the direction from which signals arrive at a receiver array. This project involves both a theoretical study of the underlying mathematical concepts and a MATLAB simulation to estimate the DOA of two distinct signal sources.

## 📖 Theoretical Concepts Covered
Based on the project report, the theoretical analysis includes:
*   **Steering Vectors:** Understanding their role in capturing the spatial and phase relationships of incoming signals and defining the signal and noise subspaces.
*   **Least Squares (LS) vs. Total Least Squares (TLS):** Analyzing the differences between these estimation techniques. The LS method is highlighted as more appropriate and computationally simpler for standard ESPRIT when dealing primarily with thermal receiver noise.
*   **ESPRIT Mathematical Derivation:** Step-by-step derivation including the estimation of the covariance matrix, Eigen-decomposition, and exploiting rotational invariance between subarrays to find the DOA.
*   **Signal Requirements & Limitations:** 
    *   Requirement for **Narrow-Band (NB)** signals.
    *   Challenges with **Coherent Signals** (requiring techniques like Matrix Pencil or spatial smoothing).
    *   Maximum number of resolvable sources ($N-1$ sources for an $N$-element uniform linear array).
    *   Geometrical constraints: The necessity of a **Uniform Linear Array (ULA)** with half-wavelength spacing and parallel subarrays (making it unsuitable for circular arrays).

## 💻 Simulation & Implementation
The MATLAB simulation implements the ESPRIT algorithm on a provided dataset:
1.  **Data Loading:** Loaded the signal data matrix corresponding to 40 receiver elements and 1000 snapshots for 2 signal sources.
2.  **Covariance Matrix & Eigendecomposition:** Computed the sample covariance matrix and extracted its eigenvalues and eigenvectors.
3.  **Subspace Estimation:** Formed matrices representing the signal subspace based on the smallest eigenvalues.
4.  **DOA Calculation:** Applied the ESPRIT equations to calculate the final arrival angles.
5.  **Results:** The simulation successfully estimated the DOA angles for the two sources at approximately **-16.05°** and **20.92°**.

## 📂 Repository Structure
*   `/data`: Contains the `.mat` file with the simulated antenna array recordings (40 receivers, 1000 snapshots).

## 👥 Authors
*   **Seyed Mohammad Erfan Bateni (400100792)**
*   Amirhossein Abedi (400101561)
*   Alireza Radfard (400101237)
