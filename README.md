# A two-stage machine learning framework for multimodal inversion of surface-wave dispersion curves

This repository contains the source code and example data for the paper:

**A two-stage machine learning framework for multimodal inversion of surface-wave dispersion curves**

## Overview

This study proposes a two-stage machine-learning framework for the inversion of multimodal Rayleigh-wave dispersion curves.

The framework consists of:

1. **Stage 1: Shear-wave velocity range estimation**  
   A DeepSets-based network is used to estimate the lower and upper bounds of the shear-wave velocity model from a variable number of similar fundamental-mode dispersion curves.

2. **Stage 2: Multimodal dispersion inversion**  
   Candidate models are selected according to the estimated velocity range. The dispersion curves are then classified by mode, corrected using frequency-band similarity and spatial consistency, and used to construct a small training dataset for multimodal inversion.

## Workflow

```text
Observed dispersion curves
          |
          v
Selection of similar fundamental-mode curves
          |
          v
Stage 1: Vs range estimation
          |
          v
Candidate model selection
          |
          v
Mode classification and correction
          |
          v
Construction of a small training dataset
          |
          v
Stage 2: Multimodal dispersion inversion
          |
          v
Shear-wave velocity model
