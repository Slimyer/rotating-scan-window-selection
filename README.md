# Pre-Imaging Control-Window Selection for Downlink-Efficient On-Orbit Geometric Calibration of Rotating-Scan Satellites

**Authors:** Zhiming Deng<sup>1</sup>, Guang Huo<sup>2</sup>, and Cheng Wei<sup>1,*</sup>  
<sup>1</sup> School of Astronautics, Harbin Institute of Technology, Harbin 150001, China  
<sup>2</sup> China Academy of Aerospace System and Innovation, Beijing 100080, China  
<sup>*</sup> Corresponding author: `weicheng@hit.edu.cn`

---

## Overview

Rotating-scan remote sensing satellites achieve both meter-level spatial resolution and ultrawide swath coverage, yet full-image downlink occupies multiple complete data-transmission orbits while ground sampling distance (GSD) expands rapidly with scan angle.

This repository accompanies our manuscript **"Pre-Imaging Control-Window Selection for Downlink-Efficient On-Orbit Geometric Calibration of Rotating-Scan Satellites"**, establishing an integrated framework for **pre-imaging ground window planning, onboard selective cropping and downlink, and post-imaging ground matching and weighted calibration**:

<p align="center">
  <img src="assets/framework.png" width="90%" alt="Pre-imaging control-window planning and on-orbit calibration framework"/>
</p>

### Key Highlights
- **Pre-Imaging Window-Planning Framework:** Formulates calibration control-data acquisition as a pre-imaging discrete subset selection problem over candidate strip windows using only nominal imaging geometry, compressing calibration downlink volume to a few thousandths of the full image (e.g., **0.15%** at $N = 24$).
- **Image-Space Area Measure & Task-Benefit Selection (IA):** Derives an image-space area measure and area-weighted task matrix $Q_{\mathrm{A}}$ aligned with spatially uniform full-swath ground positioning accuracy, propagating focal-plane measurement uncertainty through local pixel-to-ground Jacobians to directly minimize expected full-swath ground MSE $\Phi(\mathcal{S}) = \operatorname{tr}(Q_{\mathrm{A}} F_{\mathcal{S}}^{-1})$.
- **Noise-Scale Invariance & Error-Model Robustness:** Demonstrates both theoretically and experimentally that nominal imaging geometry captures the dominant cross-swath heteroscedasticity of ground observation errors without requiring complex empirical matching-noise priors.

---

## Release Roadmap

- [x] Project overview and methodological summary
- [ ] Interactive web demonstration (GitHub Pages) of step-by-step marginal task-benefit $\Delta(s \mid \mathcal{S}_t)$ evolution and dynamic window selection across budgets $N$ *(in preparation)*
- [ ] Reference Python implementation of the IA forward-selection + multi-start single-window exchange solver and anonymized nominal-geometry benchmark *(to be released upon publication)*

---

## Contact

For questions regarding this work, please contact **Zhiming Deng** (`23b918133@stu.hit.edu.cn`) or **Cheng Wei** (`weicheng@hit.edu.cn`).
