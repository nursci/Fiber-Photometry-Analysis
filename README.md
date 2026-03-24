# Fiber Photometry Standard Analysis Pipeline

This repository provides a robust Python class for processing dual-wavelength fiber photometry data (470nm GCaMP and 405nm Isosbestic). 

## Analysis Steps
Following the best practices from *Simpson et al., "Lights, fiber, action! A primer on in vivo fiber photometry" (Neuron, 2023)*:
1. **Filtering:** 2Hz Low-pass Butterworth filter.
2. **Bleaching:** Exponential decay fitting for baseline stabilization.
3. **Motion Correction:** Linear regression fitting of the 405nm reference to the 470nm signal.
4. **Normalization:** Calculation of ΔF/F and Z-Score to isolate neural transients.

## Visualization
The pipeline generates a multi-step diagnostic plot to verify signal integrity at each stage, as well as a high-resolution "Zoomed Window" to inspect calcium kinetics and sensory-evoked responses.
