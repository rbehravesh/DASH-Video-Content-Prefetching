# DASH video content prefetching 

This is an Integer Liner Programming model for DASH video content prefecing in multi-acess edge computing-enabled 5G Networks. Our contribution in this repo is modelling of video content caching and prefetching to ege points of precenses.
This repo containts the codes (MILP, Heuristic, and ML prediction) of research work with the intention to employ MEC for caching DASH video segments. 


# Download generated dataset

We have generated a huge dataset of an ns-3 simulated network to train and validate the prediction models, and to evaluate the prefetching algorithms. We generated two datasets (available at https://drive.google.com/drive/folders/1VPzpEYxs7kbtZdJYVsPm0Vbn35OB9dYz) from a simulated urban mobile network deployment scenario similar to the scenario described in the 3GPP report  [1]. We use the ns-3 DASH module implemented by Vergados et al. [2] to simulate the DASH client-server interaction for video segment requests and response. The ABR algorithm implemented on the DASH clients uses both network bandwidth and buffer occupancy information to select the bitrate of the segments requested. The set of avail- able bitrates are {1, 2.5, 5, 8, 16, 35} Mbps. Each DASH client implements a video buffer of 30 MB. It is important to emphasize here that our approach can handle any ABR at the client, as long as it can be trained on that data.


[1]. “LTE; evolved universal terrestrial radio access (E-UTRA); FDD home eNode B (HeNB) radio frequency (RF) requirements analysis,” ETSI, Sophia Antipolis, France, ETSI Rep. TR 136 921 V9.0.0, 2010. [Online]. Available: https://www.etsi.org/deliver/etsi_tr/136900_136999/ 136921/09.00.00_60/tr

[2] “An MPEG/DASH Client-Server ns3 Module.” [Online]. Available: https://github.com/djvergad/dash (Accessed: Jul. 23, 2020).

# To run the code

##Install Python3 on you system, using the instructions from here:
```
   https://wiki.python.org/moin/BeginnersGuide/Download
```
* To install Gurobi for Python and include the installation instructions in a README file on GitHub, you can follow these steps:

   ## Installing Gurobi for Python

   This project uses the Gurobi optimization library. Follow these steps to install Gurobi and set it up for Python:

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

      To verify that Gurobi is correctly installed, you can run the following Python code in your project:

      ```python
      import gurobipy as gp
      ```

   That's it! You've successfully installed Gurobi for Python. You can now use it in your project for optimization tasks.

   ```

   Make sure to replace `your_version` with the actual version of Gurobi you installed. You can also customize the README section as needed for your project.

# To run the machine learning algorithms for prediction of bitrate

This code is in a different git project that can be cloned from

git clone https://github.com/akhila-s-rao/machine-learning-for-edge-enabled-dash.git
The dataset linked above contains both the raw dataset and the pre-processed data that we used for our machine learning. If you would like to run the machine learning scripts place the folder "data" obtained from the google drive link into the cloned machine-learning-for-edge-enabled-dash directory for the machine learning scripts to be able to access them.


# Appendix with our model results

You can find here an appendix with additional tables showing result from our evaluations that have not been included in our paper for brevity

https://github.com/akhila-s-rao/machine-learning-for-edge-enabled-dash/blob/master/documentation/Appendix_Predictive_prefetching_for_edge_assisted_video_streaming.pdf


# Reference

Here are our papers describing the dataset generation process and the machine learning approach to predict video segment bitrate with the objective of predictively prefetching to the mobile edge, segments of ongoing video streams

This CNSM short paper presents initial results with a solution towards this problem

CNSM 2020 https://ieeexplore.ieee.org/document/9269054

The work was then extended with a reformulation of the solution approach with insight from our previous short paper and concluded in our journal paper

TNSM 2022 https://ieeexplore.ieee.org/document/9841468

Please refer these papers when using the results, code or dataset provided here.

