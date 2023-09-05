
# DASH Video Content Prefetching

## Overview

This repository presents an Integer Linear Programming model for DASH (Dynamic Adaptive Streaming over HTTP) video content prefetching in multi-access edge computing-enabled 5G networks. Our primary contribution here is the modeling of video content caching and prefetching to edge points of presence (PoPs). The repository contains implementations of three key components: MILP (Mixed-Integer Linear Programming), Heuristic methods, and Machine Learning-based prediction models. These components are part of a broader research effort aimed at leveraging Mobile Edge Computing (MEC) for caching DASH video segments.

## Download the Generated Dataset

We have generated a comprehensive dataset based on an ns-3 simulated network. This dataset serves multiple purposes, including training and validating prediction models and evaluating prefetching algorithms. The dataset is available [here](https://drive.google.com/drive/folders/1VPzpEYxs7kbtZdJYVsPm0Vbn35OB9dYz).

### Dataset Details

- We simulated an urban mobile network deployment scenario similar to the one described in the 3GPP report [1].
- We used the ns-3 DASH module implemented by Vergados et al. [2] to simulate the DASH client-server interaction for video segment requests and responses.
- The Adaptive Bitrate (ABR) algorithm implemented on the DASH clients considers both network bandwidth and buffer occupancy information to select the bitrate of the requested video segments. The set of available bitrates is {1, 2.5, 5, 8, 16, 35} Mbps, and each DASH client has a video buffer of 30 MB.
- It's worth noting that our approach can accommodate any ABR algorithm at the client, provided it can be trained on the available data.

[1]. [3GPP Report](https://www.etsi.org/deliver/etsi_tr/136900_136999/136921/09.00.00_60/tr)
[2]. [MPEG/DASH Client-Server ns3 Module](https://github.com/djvergad/dash) (Accessed: Jul. 23, 2020).

## Getting Started

### Prerequisites

To run this project, you'll need Python 3 installed on your system. You can download and install Python 3 by following the instructions [here](https://wiki.python.org/moin/BeginnersGuide/Download).

### Installing Gurobi for Python

This project utilizes the Gurobi optimization library. Follow these steps to install Gurobi and set it up for Python:

1. **Obtain a Gurobi License:**
   - You can request a free academic license or purchase a commercial license from the [Gurobi website](https://www.gurobi.com/downloads/request-an-academic-license/).

2. **Download and Install Gurobi:**
   - Download the Gurobi optimizer for your platform (Windows, macOS, Linux) from the [Gurobi download page](https://www.gurobi.com/downloads/gurobi-software/).
   - Follow the installation instructions provided for your platform.

3. **Install Gurobi Python Interface:**
   - Open a terminal or command prompt.
   - Use pip to install the Gurobi Python package. Replace `your_version` with the version of Gurobi you installed:

   ```bash
   pip install gurobipy==your_version
   ```

4. **Verify Installation:**
   - To ensure that Gurobi is correctly installed, run the following Python code in your project:

   ```python
   import gurobipy as gp
   ```

You have now successfully installed Gurobi for Python and can use it for optimization tasks in your project.

### Running Machine Learning Algorithms for Bitrate Prediction

The code for machine learning-based bitrate prediction is available in a separate Git repository, which you can clone using the following command:

```bash
git clone https://github.com/akhila-s-rao/machine-learning-for-edge-enabled-dash.git
```

To run the machine learning scripts, place the "data" folder obtained from the Google Drive link mentioned above into the cloned "machine-learning-for-edge-enabled-dash" directory. This allows the machine learning scripts to access the necessary data.

## Appendix - Model Results

Additional tables and results from our evaluations, not included in the main paper for brevity, can be found in the [Appendix](https://github.com/akhila-s-rao/machine-learning-for-edge-enabled-dash/blob/master/documentation/Appendix_Predictive_prefetching_for_edge_assisted_video_streaming.pdf).

## References

Please refer to the following papers when using the results, code, or dataset provided in this repository:

- [CNSM 2020](https://ieeexplore.ieee.org/document/9269054)
- [TNSM 2022](https://ieeexplore.ieee.org/document/9841468)

These papers describe the dataset generation process and the machine learning approach for predicting video segment bitrates, with the objective of predictively prefetching to the mobile edge.

You can copy and paste this code into your README file on GitHub, and make any necessary adjustments or customizations to match your project's details.
