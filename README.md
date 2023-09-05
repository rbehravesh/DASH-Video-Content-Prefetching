# DASH Video Content Prefetching 

This is an Integer Liner Programming model for DASH video content prefecing in multi-acess edge computing-enabled 5G Networks. Our contribution in this repo is modelling of video content caching and prefetching to ege points of precenses.
This repo containts the codes (MILP, Heuristic, and ML prediction) of research work with the intention to employ MEC for caching DASH video segments. 


# Download Generated Dataset

We have generated a huge dataset of an ns-3 simulated network to train and validate the prediction models, and to evaluate the prefetching algorithms. We generated two datasets (available at https://drive.google.com/drive/folders/1VPzpEYxs7kbtZdJYVsPm0Vbn35OB9dYz) from a simulated urban mobile network deployment scenario similar to the scenario described in the 3GPP report  [1]. We use the ns-3 DASH module implemented by Vergados et al. [2] to simulate the DASH client-server interaction for video segment requests and response. The ABR algorithm implemented on the DASH clients uses both network bandwidth and buffer occupancy information to select the bitrate of the segments requested. The set of avail- able bitrates are {1, 2.5, 5, 8, 16, 35} Mbps. Each DASH client implements a video buffer of 30 MB. It is important to emphasize here that our approach can handle any ABR at the client, as long as it can be trained on that data.


[1]. “LTE; evolved universal terrestrial radio access (E-UTRA); FDD home eNode B (HeNB) radio frequency (RF) requirements analysis,” ETSI, Sophia Antipolis, France, ETSI Rep. TR 136 921 V9.0.0, 2010. [Online]. Available: https://www.etsi.org/deliver/etsi_tr/136900_136999/ 136921/09.00.00_60/tr

[2] “An MPEG/DASH Client-Server ns3 Module.” [Online]. Available: https://github.com/djvergad/dash (Accessed: Jul. 23, 2020).
