# Multi-Agent Digital Twins for Strategic Decision-Making using Active Inference

This repository provides all the code required to reproduce the results presented in the paper:

**“Multi-Agent Digital Twins for Strategic Decision-Making using Active Inference”**

## Code Availability and Dependencies

This project builds upon a custom fork of the pymdp library:

- Original repository: https://github.com/infer-actively/pymdp  
- Fork used in this work: https://github.com/Franceeeee/pymdp  

The fork introduces the following extensions:

1. **`shared_control_groups`**  
   Allows explicit specification of which hidden states are influenced by the same control actions.

2. **`scale_state`**  
   Introduces a scaling factor to modulate the contribution of *state information gain* in the inference process.

All experiments in this repository rely on this modified version of the library.

## Repository Structure

The repository contains five Jupyter notebooks, each corresponding to a specific experimental setting:

### 1. `two_player_classic.ipynb`

- Baseline two-player setting  
- Well-posed Generative Model (GM) for both firms  
- Generative Process (GP) with **double buyer reduction**

This notebook serves as the reference implementation of the duopoly scenario.

---

### 2. `two_player_precision_classic.ipynb`

- Same structure as the baseline two-player model  
- **Firm 2 operates with increased precision** (i.e., reduced variance)  
- Generative Process with **double buyer reduction**

Used to analyze the effect of asymmetric uncertainty under the original GP specification.

---

### 3. `two_player_precision.ipynb`

- **Firm 2 with increased precision**  
- **Simplified Generative Process** with a **single buyer reduction**

This configuration isolates the role of GP simplification in combination with asymmetric precision.

---

### 4. `three_player.ipynb`

- Three-player extension of the model  
- All firms use **well-designed Generative Models**  
- **Baseline Generative Process**

Provides a multi-agent extension of the core framework.

---

### 5. `three_player_precision.ipynb`

- Three-player setting  
- **Firm 2 with increased precision**  
- Baseline Generative Process

Used to study how asymmetric precision affects strategic interaction in a multi-agent environment.

