# 🏇 Awesome Wi-Fi Sensing Generalization

[Fei Wang](https://scholar.google.com/citations?user=LKPpmXQAAAAJ), [Tingting Zhang](https://scholar.google.com/citations?user=R7kxvQkAAAAJ), [Wei Xi](https://scholar.google.com/citations?user=Xt3XP-EAAAAJ), [Han Ding](https://scholar.google.com/citations?user=0sLAHGUAAAAJ), [Ge Wang](https://scholar.google.com/citations?user=ngEGALwAAAAJ), [Di Zhang](https://scholar.google.com/citations?user=HKC6ecEAAAAJ), [Yuanhao Cui](https://scholar.google.com/citations?user=ShAefLUAAAAJ), [Fan Liu](https://scholar.google.com/citations?user=kj2PE40AAAAJ), [Jinsong Han](https://scholar.google.com/citations?user=BST50KwAAAAJ&hl=en&oi=ao), [Jie Xu](https://scholar.google.com/citations?user=HPUG2jwAAAAJ), [Tony Xiao Han](https://scholar.google.com/citations?user=cqvSehcAAAAJ), **A Survey on Wi-Fi Sensing Generalizability: Taxonomy, Techniques, Datasets, and Future Research Prospects**, IEEE Communications Surveys & Tutorials, 2026

**Sensing Dataset Platform:** https://sdp8.org/

```
@article{wang2026wifisurvey,
  author    = {Fei Wang and Tingting Zhang and Wei Xi and Han Ding and Ge Wang and Di Zhang and Yuanhao Cui and Fan Liu and Jinsong Han and Jie Xu and Tony Xiao Han},
  title     = {A Survey on Wi-Fi Sensing Generalizability: Taxonomy, Techniques, Datasets, and Future Research Prospects},
  journal   = {IEEE Communications Surveys \& Tutorials},
  year      = {2026}
}
```


![fig3](https://github.com/user-attachments/assets/95ff3b85-0965-433c-95dc-449c87cda4e1)
Fig.3: Growth of research in Wi-Fi sensing generalizability: from a handful of studies between year of 2015 and 2018 to a surge of publications since 2019. We employed a linear regression to fit the growth trend. In the figure, the $R^2$ score indicates the correlation between the estimated results and the ground truth, where a value closer to 1 denotes a higher degree of model fitting. (We selected one representative paper per year based on the highest citation count, ensuring each choice employs a technical approach distinct from those featured in previous years.)


> ### **Highlight**
>
> While this survey focuses on Wi-Fi sensing, it is worth noting that many of the taxonomy and generalization challenges discussed herein are also applicable to millimeter-wave radar–based human sensing, which has gained increasing attention with the availability of commodity radars. Although mmWave radar relies on different signal representations, such as range–Doppler or range–angle maps rather than Wi-Fi CSI, it faces similar fundamental challenges related to device heterogeneity, human body diversity, and environment diversity.  
>
> For example, variations in radar hardware configurations and antenna arrays resemble device heterogeneity in Wi-Fi sensing; differences in human body shape, motion patterns, and orientation affect radar reflections in a manner analogous to CSI-based sensing; and environmental factors such as clutter, multipath, and deployment geometry similarly impact sensing robustness.  
>
> As a result, learning paradigms and deployment strategies aimed at improving generalization, such as multi-view sensing, large-scale in-the-wild datasets, domain adaptation, and continual learning, can be conceptually extended to millimeter-wave radar sensing, despite differences in signal modality.



---

## :turtle: Tools

| Name | max. MIMO | 802.11 support | max. # subcarriers | max. bandwidth | Wi-Fi | Download Link |
|---|---|---|---|---|---|---|
| Intel CSITool | 2×2 | n | 60 | 40 MHz | CSI | https://dhalperi.github.io/linux-80211n-csitool/ |
| Atheros CSITool | - | n | 114 | 40 MHz | CSI | https://github.com/xieyaxiongfly/Atheros-CSI-Tool |
| Nexmon CSITool | 4×4 | n/ac | 256 | 80 MHz | CSI | https://github.com/seemoo-lab/nexmon_csi |
| Wi-ESP | 2×2 | b/g/n/ac | 64 | 40 MHz | CSI | https://github.com/wrlab/Wi-ESP |
| ZTE CSITool | 3×2 | n/ac/ax | 512 | 160 MHz | CSI | https://github.com/WiFiZTE2025/ZTE_WiFi_Sensing |
| PicoScenes | 4×4 | a/g/n/ac/ax/be | 1024 | 320 MHz | CSI | https://ps.zpj.io/ |
| BFM-Tool | 4×4 | ac/ax | 512 | 160 MHz | BFI | https://github.com/Enze-Yi/BFM-tool |

---

## :dog: Datasets 

<img width="1781" height="746" alt="fig17" src="https://github.com/user-attachments/assets/aeb2a618-6cc8-4b60-a928-93cc69c80f66" />
Fig. 17: Bubble chart of public Wi-Fi sensing datasets, where the bubble size indicates the number of samples and the vertical axis represents the number of classes. For visual clarity, datasets with extreme values, such as SignFi (296 classes) and CSI-Bench (over 1,000,000 samples), are excluded from the plot. Besides, datasets like WiFiTAD, MM-Fi, and XRFv2, which collect continuous sequences over time without clear per-sample annotations, are also not included due to the ambiguity in estimating their sample counts.

<br>
<br>

Table VII: Wi-Fi Datasets. The main results column mainly denotes the in-domain results from the original publications.
| ID | Dataset | Main Domain Information | Device Setting | Highlight | Main Results | Download Link |
|---|---|---|---|---|---|---|
| **Action Recognition** |
| 1 | [XRF55](https://aiotgroup.github.io/XRF55/) | 4 environments, 39 participants, 55 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, 55 actions | 87.26% |https://aiotgroup.github.io/XRF55/ |
| 2 | [BullyDetect](https://github.com/aiotgroup/WiFi-BullyDetect) | 8 environments, 20 paired participants, 7 actions | 1Tx, 1Rx, 20MHz, 5GHz | Bullying actions | 90.4% |https://github.com/aiotgroup/WiFi-BullyDetect|
| 3 | [WiSDA](https://ieeexplore.ieee.org/abstract/document/10756643/) | 1 environments, 3 participants, 6 actions | 1Tx, 1Rx, 20MHz | Widar3.0-like | 99.5% |https://www.researchgate.net/publication/385918549_WiSDA_Subdomain_Adaptation_Human_Activity_Recognition_Method_Using_Wi-Fi_Signals|
| 4 | [WiNDR](https://www.sciencedirect.com/science/article/pii/S0140366423004747) | 1 environments, 3 participants, 5 actions, 24 orientation | 1Tx, 1Rx, 20MHz, 5GHz | Full 360° coverage | 78%-92% |https://gitlab.com/yuxiqin/direction-independent|
| 5 | [WiMANS](https://link.springer.com/chapter/10.1007/978-3-031-72946-1_5) | 3 environments, 6 participants, 9 actions | 1Tx, 1Rx, 20MHz, 2.4/5GHz | Multi-person | 89.1%-96.6% |https://github.com/huangshk/WiMAN|
| 6 | [WiGuesture](https://ieeexplore.ieee.org/abstract/document/10620769/) | 1 environments, 8 participants, 6 actions | 1Tx, 1Rx, 100Hz, 2.4GHz | ESP32S3 | 92.57% |https://github.com/RS2002/CSI-BERT|
| 7 | [RoGER](https://ieeexplore.ieee.org/abstract/document/10625160/) | 2 environments, 4 participants, 6 actions, 4 orientation | 1Tx, 2Rx, 20MHz, 2.437GHz | AR9580 | 94.84%-99.71% |http://bisuzhi.cn/Sensedata.html|
| 8 | [ImgFi](https://ieeexplore.ieee.org/abstract/document/10190332/) | 1 environments, 5 participants, 6 actions | 1Tx, 1Rx, 20MHz | Converted to images | 99.8% |https://ieeexplore.ieee.org/document/10190332|
| 9 | [ResMon](https://ieeexplore.ieee.org/abstract/document/10147361/) | 2 environments, 3 areas, 6 participants, 4 actions | 1Tx, 1Rx, 20/40MHz, 2.4/5GHz | Cross-band test | 83.80%-89.67% |http://bisuzhi.cn/Sensedata.html|
| 10 | [Meneghello et al.](https://ieeexplore.ieee.org/abstract/document/10144501/) | 6 environments, 4 participants, 7 actions | 1Tx, 1Rx, 80MHz, 5.21GHz | 80MHz | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| 11 | [Demrozi et al.](https://www.techrxiv.org/doi/full/10.36227/techrxiv.22284421) | 2 environments, 6 participants, 6 actions | 2Tx, 2Rx, 2.4GHz | Nexmon firmware | 99.3% |https://www.techrxiv.org/doi/full/10.36227/techrxiv.22284421.v1|
| 12 | [MM-Fi](https://ntu-aiot-lab.github.io/mm-fi) | 4 environments, 40 participants, 27actions | 1TX, 1RX, 20MHz, 5GHz | Multimodal | not reported |https://ntu-aiot-lab.github.io/mm-fi|
| 13 | [NTU-Fi HAR](https://ieeexplore.ieee.org/abstract/document/9667414/) | 1 environments, 20 participants, 6 actions | 1Tx, 1Rx, 40MHz, 5GHz | TP-Link N750 | 98.6% |https://github.com/xyanchen/WiFi-CSI-Sensing-Benchmark|
| 14 | [FallDar](https://ieeexplore.ieee.org/abstract/document/9816096/) | 4 environments, 6 locations, 6 participants, fall & normal | 1Tx, 1Rx, 1000Hz, 5GHz | 6 months | 5.7% FAR |http://www.sdp8.net/Dataset?id=dfe4621e-4774-4ef4-b064-e4a082c12335|
| 15 | [ReWis](https://ieeexplore.ieee.org/abstract/document/9842828/) | 3 environments, 2 participants, 4 actions | 1Tx, 3Rx, 20/80MHz, 5GHz | 80MHz | 78.25%-99.82% |https://github.com/niloobah/ReWiS|
| 16 | [OPERAnet](https://www.nature.com/articles/s41597-022-01573-2) | 2 environments, 6 participants, 6 actions | 1Tx, 2Rx, 5GHz | Multimodal | 71%-100% |https://springernature.figshare.com/collections/A_Comprehensive_Multimodal_Activity_Recognition_Dataset_Acquired_from_Radio_Frequency_and_Vision-Based_Sensors/5551209/1|
| 17 | [SHARP](https://github.com/francescamen/SHARP) | 3 environments, 4 locations, 3 participants, 7 actions | 1Tx, 1Rx, 80MB, 5GHz | 80MHz | 95.99%-99.79% |https://github.com/francescamen/SHARP|
| 18 | [CSI-HAR-Dataset](https://www.mdpi.com/1424-8220/21/21/7225) | 1 environments, 3 participants, 7 actions | 1Tx, 1Rx, 20MHz, 5GHz | 802.11ac | 95.5% |https://github.com/parisafm/CSI-HAR-Dataset|
| 19 | [CSIDA](https://ieeexplore.ieee.org/abstract/document/9542947/) | 2 environments, 5 locations, 5 participants, 6 actions | 1Tx, 1Rx, 40MHz, 5GHz | 114 subcarriers | 90.10%±1.03% |https://github.com/Zhang-xie/WiGr|
| 20 | [RISE](https://github.com/jiaojiao1234/RISE) | 2 environments, 6 participants, 6 actions | 1Tx, 1Rx | multi-rf devices | 93.9%-100% |https://github.com/jiaojiao1234/RISE|
| 21 | [HTHI](https://www.sciencedirect.com/science/article/pii/S235234092030562X) | 1 environment, 40 paired, 12 actions | 2Tx, 3Rx, 20MHz, 2.4GHz | Human-human actions | not reported |https://data.mendeley.com/datasets/3dhn4xnjxw/1|
| 22 | [DeepSeg](https://github.com/ChunjingXiao/DeepSeg) | 1 environment, 5 participants, 10 actions | 1Tx, 3Rx | fine-/coarse-grained actions | 94% |https://github.com/ChunjingXiao/DeepSeg|
| 23 | [RF-Net](https://github.com/di0002ya/RFNet) | 6 environments, 11 participants, 6 actions | 2 Tx-Rx pairs, 20MHz | 120 environment | ≈ 80% |https://github.com/di0002ya/RFNet|
| 24 | [Baha’A et al.](https://www.sciencedirect.com/science/article/pii/S2352340920314165) | 3 environments, 30 participants, 12 actions | 1Tx, 3Rx, 20MHz, 2.4GHz | LOS/NLOS | not reported |http://www.sdp8.net/Dataset?id=dfe4621e-4774-4ef4-b064-e4a082c12335|
| 25 | [Widar 3.0](https://tns.thss.tsinghua.edu.cn/widar3.0/) | 3 environments, 5 locations, 5 orientations, 16 participants, 16 actions | 1Tx, 6Rx, 20MHz, 5.825GHz | Rich domains | 92.7%-92.9% |https://tns.thss.tsinghua.edu.cn/widar3.0/|
| 26 | [ARIL](https://github.com/geekfeiw/ARIL) | 16 locations, 1 participants, 6 actions | 1Tx, 1Rx, 20MHz, 2.4GHz | USRP data, clean phase | 89.57% |https://github.com/geekfeiw/ARIL|
| 27 | [WiAR](https://github.com/linteresa/WiAR) | 3 environments, 10 participants, 16 actions | 1Tx, 1Rx, 20MHz, 5GHz | RSSI and CSI | 90.62%-96.25% |https://github.com/linteresa/WiAR|
| 28 | [SAR](https://dl.acm.org/doi/abs/10.1145/3359427.3361913) | 1 environment, 9 participants, 6actions | 2-3Tx, 3Rx, 20MHz, 2.4GHz | 6 days | 60%-100% |https://data.4tu.nl/articles/_/12692816/1|
| 29 | [FallDeFi](https://github.com/dmsp123/FallDeFi) | 5 environments, 3 participants, 9 actions | 2Tx, 2Rx, 20MHz, 5.2GHz | Fall detection | 80.10%-88.90% |https://github.com/dmsp123/FallDeFi|
| 30 | [SignFi](https://github.com/yongsen/SignFi) | 2 environments, 5 participants, 276 gestures | 3Tx, 1Rx, 20MHz, 5GHz | 276 ASL Gestures | 94.81%-98.91% |https://github.com/yongsen/SignFi|
| 31 | [CrossSense](https://github.com/nwuzj/CrossSense/) | 3 environments, 15 locations, 100 participants, 40 actions | 1Tx, 1Rx, 20MHz, 5GHz | 100 participants | 90% |Agreement required https://github.com/nwuzj/CrossSense/|
| 32 | [Yousef et al.](https://ieeexplore.ieee.org/abstract/document/8067693/) | 1 environments, 6 participants, 6 actions | 1Tx, 1Rx, 20MHz, 5GHz | Fall | 81%-97% |https://github.com/ermongroup/Wifi_Activity_Recognition|
| **Gait Recognition** |
| 33 | [NTU-Fi HumanID](https://ieeexplore.ieee.org/abstract/document/9726794/) | 2 environments, 20 participants, walking | 1Tx, 1Rx, 40MHz, 5GHz | TP-Link N750 | 86.29&-98.34% |https://github.com/xyanchen/WiFi-CSI-Sensing-Benchmark|
| 20 | [RISE](https://github.com/jiaojiao1234/RISE/) | 3 environments, 15 participants | 1Tx, 1Rx | multi-rf devices | 97.6% |https://github.com/jiaojiao1234/RISE/|
| 34 | [GaitID](https://link.springer.com/chapter/10.1007/978-3-030-59016-1_60) | 2 environments, 11 participants, 8 directions | 1Tx, 6Rx | 8 directions | 61%-100% |http://www.sdp8.net/Dataset?id=87a65da2-18cb-4b8f-a1ec-c9696890172b|
| 31 | [CrossSense](https://github.com/nwuzj/CrossSense) | 3 environments, 100 participants | 1Tx, 1Rx, 20MHz, 5GHz | 100 participants | 80% |Agreement required https://github.com/nwuzj/CrossSense|
| **Pose Estimation** |
| 35 | [XRFv2](https://github.com/aiotgroup/XRFV2) | 3 environments, 16 participants, 30 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, continuous actions | not reported |https://github.com/aiotgroup/XRFV2|
| 36 | [Person-in-WiFi 3D](https://aiotgroup.github.io/Person-in-WiFi-3D/) | 3 environments, 7 participants, 8actions | 1Tx, 3Rx, 20MHz, 5GHz | Multi-person | 107.2mm MPJPE |https://aiotgroup.github.io/Person-in-WiFi-3D/|
| 1 | [XRF55](https://aiotgroup.github.io/XRF55/) | 4 environments, 39 participants, 55 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, 55 actions | not reported |https://aiotgroup.github.io/XRF55/|
| 12 | [MM-Fi](https://ntu-aiot-lab.github.io/mm-fi) | 4 environments, 40 participants, 27 actions | 20MHz, 5GHz | Multimodal | 197.1mm MPJPE |https://ntu-aiot-lab.github.io/mm-fi|
| **Indoor Localization** |
| 37 | [MetaLoc](https://github.com/StatFusion/MetaLoc) | 2 environments, 180 locations | 3Tx, 1Rx, 20MHz, 5GHz | RSSI and CSI | 2.07±1.11m error |https://github.com/StatFusion/MetaLoc|
| 38 | [Chen and Chang](https://ieeexplore.ieee.org/document/9839217/) | 2 environments, 16 locations | 2Tx, 2Rx | CSI fingerprints | 49.47%-90.44% |https://github.com/BingJiaChen/few-shot-indoor-localization|
| 26 | [ARIL](https://github.com/geekfeiw/ARIL) | 1 environments, 16 locations, 1 participants, 6 actions | 1Tx, 1Rx, 20MHz, 2.4GHz | USRP data, clean phase | 95.68% |https://github.com/geekfeiw/ARIL|
| **Crowd Counting** |
| 39 | SDP| 4 scenarios | multi-APs, 80/160MHz, 5GHz | 0-2 people | not reported |https://sdp8.org/Dataset?id=277beeba-afdc-4bb1-8b47-88fa366fb27d|
| 40 | [DASECount](https://ieeexplore.ieee.org/abstract/document/9996126/) | 2 environments, 2 scenarios (NLOS/LOS), 3 motions | 1Tx, 1Rx, 40MHz, 2.4GHz | 0-8 people | 93.29%-99.17% |http://bisuzhi.cn/Sensedata.html|
| 10 | [Meneghello et al.](https://ieeexplore.ieee.org/abstract/document/10144501/)  | 1 environments, 10 participants | 1Tx, 1Rx, 80MHz, 5.21GHz | 1-10 people | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| **Temporal Action Localization, Action Summarization** |
| 35 | [XRFv2](https://github.com/aiotgroup/XRFV2) | 3 environments, 16 participants, 30 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, continuous actions | 78.74 mAP |https://github.com/aiotgroup/XRFV2|
| 41 | [WiFiTAD](https://github.com/AVC2-UESTC/WiFiTAD) | 1 environment, 3 participants, 7 actions | 1Tx, 1Rx, 5GHz | Continuous actions | 74.5 mAP |https://github.com/AVC2-UESTC/WiFiTAD|
| **Multiple Sub-Datasets** |
| 42 | [CSI-Bench](https://ai-iot-sensing.github.io/projects/project.html) | 26 environments, 35 participants | 16 device configuration | In-the-wild data, 461 hours | 94.88% fall detection, etc. |https://ai-iot-sensing.github.io/projects/project.html|
| 10 | [Meneghello et al.](https://ieeexplore.ieee.org/abstract/document/10144501/)  | 7 environments, 13 participants | 1Tx, 1Rx, 80MHz, 5.21GHz | Three tasks, 80MHz | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| 43 | [CSI-Net](https://github.com/geekfeiw/CSI-Net) | 1 environments, 5 positions, 30 participants | 1Tx, 1Rx, 20MHz, 5GHz | Four tasks, Biometrics | 96.67% fall detection, etc. |https://github.com/geekfeiw/CSI-Net|

### 🦙 Latest Dataset Update 

**You are welcome to contribute datasets via issues or pull requests.**

1. Yuan, D., Zhang, X., Hou, W., Lyu, S., Yu, Y., Yu, L. J. T., ... & Wu, C. [OctoNet: A Large-Scale Multi-Modal Dataset for Human Activity Understanding Grounded in Motion-Captured 3D Pose Labels](https://aiot-lab.github.io/OctoNet/). In The Thirty-ninth Annual Conference on Neural Information Processing Systems Datasets and Benchmarks Track. 2025. 

---

## 🐼 Papers

<img width="1027" height="1098" alt="image" src="https://github.com/user-attachments/assets/6c7b1fb6-0cb3-41da-9d76-e52896d1f720" />
Fig 4: We systematically review and categorize nearly a decade of research on Wi-Fi sensing generalization, covering over 200 publications since 2015. Distinct from previous surveys, we organize the literature along a four-stage sensing pipeline—device deployment, signal preprocessing, feature learning, and model deployment.


## Stage 1: 🐘 Experimental Setup 

<img width="1924" height="420" alt="image" src="https://github.com/user-attachments/assets/f1cb9257-4b60-4ef8-a0e2-73745e4619ff" />
Fig5: In the experimental setup stage, Wi-Fi generalization can be enhanced by distributing antennas to mitigate the impact of user orientation, deploying devices more widely or optimizing their placement to increase coverage, and collecting more diverse datasets to support the training of more robust and generalizable models.

<br>

Table II: Comparison of Experimental Setup Strategies for Enhanced Generalization.
| Category | Pros (Advantages) | Cons (Limitations) | Generalization Mechanism | Best-fit Scenarios |
|-----------|------------------|--------------------|---------------------------|--------------------|
| **Distributed Antennas** <br> (Qin et al., 2024; Qin et al., 2023; Wang et al., 2018) | Achieves direction-agnostic sensing with single device pairs; minimal additional hardware cost. | Requires manual antenna placement; limited coverage in large-scale areas. | Introduces angular diversity by capturing signals from multiple viewpoints, reducing sensitivity to human orientation and body aspect angle. | Gesture and activity recognition tasks where user orientation varies but deployment scale is limited. |
| **Distributed Devices** <br> (Bahadori et al., 2022; Zheng et al., 2019; Xiao et al., 2021; Wu et al., 2021) | Provides high spatial resolution; reduces blind spots and mitigates multipath occlusions. | High deployment cost; complex synchronization and calibration across devices. | Exploits spatial diversity by observing heterogeneous signal responses across locations, improving robustness to environmental variations. | Large indoor spaces or complex layouts requiring robust cross-location generalization. |
| **Scaling Up Dataset** <br> (Wang et al., 2024; Zheng et al., 2019; Zhang et al., 2023; Yang et al., 2024; Zhu et al., 2025) | Enables models to learn implicit invariances; improves robustness and supports few-shot transfer. | Labor-intensive data collection; increased storage and training computation cost. | Enhances population-level generalization by exposing models to diverse human body types, motion patterns, and interaction styles. | Data-driven systems targeting user-independent sensing across diverse populations and activities. |

### Distributed Antennas

\[63\] Y . Qin, S. Sigg, S. Pan, and Z. Li, "Direction-agnostic gesture
recog- nition system using commercial wifi devices,"Computer Communications, vol. 216, pp. 34--44, 2024. [paper](https://www.sciencedirect.com/science/article/pii/S0140366423004747)

\[64\] Y . Qin, S. Pan, and Z. Li, "Cross-domain extendable gesture
recognition system using wifi signals,"Electronics Letters, vol. 59, no.
16, p. e12931, 2023. [paper](https://ietresearch.onlinelibrary.wiley.com/doi/full/10.1049/ell2.12931)

\[65\] F. Wang, W. Gong, and J. Liu, "On spatial diversity in wifi-based
human activity recognition: A deep learning-based approach,"IoT-J, 
vol. 6, no. 2, pp. 2035--2047, 2018. [paper]()


### Distributed Devices

\[66\] N. Bahadori, J. Ashdown, and F. Restuccia, "Rewis: Reliable wi-fi
sensing through few-shot multi-antenna multi-receiver csi learning," in
WoWMoM. IEEE, 2022, pp. 50--59. [paper]()

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325. [paper]()

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219. [paper]()

\[69\] D. Wu, Y . Zeng, R. Gao, S. Li, Y . Li, R. C. Shah, H. Lu, and D.
Zhang, "Witraj: Robust indoor motion tracking with wifi signals,"IEEE
TMC, vol. 22, no. 5, pp. 3062--3078, 2021. [paper]()

### Scaling Up Dataset

\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024. [paper]()

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325. [paper]()

\[71\] Y . Zhang, Y . Yin, Y . Wang, J. Ai, and D. Wu, "Csi-based
location- independent human activity recognition with parallel
convolutional networks,"Computer Communications, vol. 197, pp. 87--95,
2023. [paper]()

\[72\] J. Yang, H. Huang, Y . Zhou, X. Chen, Y . Xu, S. Yuan, H. Zou, C.
X. Lu, and L. Xie, "Mm-fi: Multi-modal non-intrusive 4d human dataset
for versatile wireless sensing,"NeurIPS, vol. 36, 2024. [paper]()

\[73\] G. Zhu, Y . Hu, W. Gao, W.-H. Wang, B. Wang, and K. Liu, "Csi-
bench: A large-scale in-the-wild dataset for multi-task wifi sensing,"
arXiv preprint arXiv:2505.21866, 2025. [paper]()

> ### **Key Takeaways and Lessons Learned: Experimental Setup**
>
> - **Structural Invariance through Spatial Diversity:**  
>   Distributed antenna topologies (e.g., staggered or circular layouts) and multi-device configurations (e.g., 1-TX with 4–6 RXs) provide a physical-layer solution to orientation sensitivity. This “structural invariance” ensures multi-view signal observations that effectively mitigate body-shadowing and occlusion.
>
> - **Placement as a Robustness Multiplier:**  
>   Optimizing the geometric placement of transmitters and receivers is critical for capturing spatially heterogeneous channel responses. Strategic layout design not only maximizes the sensing range but also significantly reduces the impact of environmental multipath interference.
>
> - **Natural Invariance through Data Scaling:**  
>   A key lesson from large-scale datasets (e.g., XRF55, CSI-Bench) is the existence of a quantitative threshold where models begin to exhibit “natural” invariance. Massive data exposure allows models to inherently decouple human motion from specific propagation conditions, facilitating easier adaptation to novel domains.
>
> - **Exploiting Diversity to Counter Heterogeneity:**  
>   To overcome device heterogeneity, moving from single-link to multi-link coordinated sensing is essential. Distributed setups exploit spatial and hardware diversity to average out the unique radio artifacts and hardware imperfections of individual commercial Wi-Fi chipsets.



## Stage 2: :snail: Signal Preprocessing
<img width="2079" height="712" alt="image" src="https://github.com/user-attachments/assets/cec677eb-88e3-434e-b8b8-9dcd3cf465c9" />
Fig 6: Signal Preprocessing Stage

<br>

Table III: Comparison of Signal Preprocessing Techniques for Wi-Fi Sensing Generalization.
| Category | Pros (Advantages) | Cons (Limitations) | Generalization Mechanism | Best-fit Scenarios |
|-----------|------------------|--------------------|---------------------------|--------------------|
| **Signal Analysis** <br>(Lu et al., 2019; Zhou et al., 2022; Yang et al., 2023; Zhuo et al., 2023; Abuhoureyah et al., 2024) | Effective for noise removal, trend extraction, and background subtraction. | Often computationally intensive; may lose non-linear motion details. | Extracting motion-related components via signal decomposition (e.g., PCA, ICA, SSA). | Stable environments; offline analysis; scenarios requiring strong denoising. |
| **Handcrafted** <br>(Meng et al., 2021; Huang et al., 2021; Gao et al., 2022; Zhang et al., 2022; Yu et al., 2023; Zhang et al., 2022; Peng et al., 2023; Wang et al., 2024; Ding et al., 2024; Peng et al., 2024; Bu et al., 2018; Zhang et al., 2023) | High interpretability; robust to specific interference (e.g., CCI) and phase errors. | Sensitive to hardware variations and chipset-specific phase noise. | Designing invariant indicators (e.g., Phase Difference, IQ curvature) to bypass shifts. | Resource-constrained systems; applications demanding interpretability and robustness. |
| **Motion Indicators** <br>(Meneghello et al., 2022; Zhao et al., 2024; Yin et al., 2021; Feng et al., 2022; Niu et al., 2021; Chen et al.; Li et al.; Van et al., 2023; Van et al., 2022; Wu et al., 2021; Zheng et al., 2019; Zhang et al., 2023; Yang et al., 2023; Shi et al., 2023; Bulugu et al., 2023; Zhang et al., 2020; Xiao et al., 2021; Chi et al., 2024; Gao et al., 2021; Shi et al., 2020; Wang et al., 2022; Wu et al., 2016; Wang et al., 2016; Qin et al., 2024; Zhang et al., 2019; Zhang et al., 2021; Zhang et al., 2019; Zhu et al., 2024) | High-level physical abstraction; achieves environment and location independence. | Requires high-resolution CSI or specific multi-antenna configurations. | Mapping signals to body-coordinate velocity/speed profiles (e.g., BVP, DFS). | Cross-environment deployment; user-independent sensing; mobility-centric tasks. |
| **Angle Indicators** <br>(Li et al., 2020; Han et al., 2023; Ren et al., 2022) | Provides precise spatial geometry; robust for trajectory tracking and Re-ID. | Performance is sensitive to antenna array calibration and layout. | Utilizing spatial consistency (e.g., AoA, ADoA) to digitize human posture and movement. | Localization, tracking, and identification tasks with calibrated antenna arrays. |

### Signal Analysis Methods
\[74\] Y . Lu, S. Lv, and X. Wang, "Towards location independent gesture
recognition with commodity wifi devices,"Electronics, vol. 8, no. 10,
p. 1069, 2019. [paper]()

\[75\] R. Zhou, Z. Gong, K. Tang, B. Zhou, and Y . Cheng, "Device-free
cross location activity recognition via semi-supervised deep
learning,"Neural Computing and Applications, vol. 34, no. 12, pp. 10
189--10 203, 2022. [paper]()

\[76\] J. Yang, Y . Liu, Y . Wu, P. Yang, and Z. Liu, "Gait-enhance:
Robust gait recognition of complex walking patterns based on wifi csi,"
inSmart World Congress. IEEE, 2023, pp. 1--9. [paper]()

\[77\] H. Zhuo, X. Wu, Q. Zhong, and H. Zhang, "Position-free breath
detection during sleep via commodity wifi,"IEEE Sensors Journal, 2023. [paper]()

\[78\] F. Abuhoureyah, S. K. Swee, and W. Y . Chiew, "Multi-user human
activity recognition through adaptive location-independent wifi signal
characteristics,"IEEE Access, 2024. [paper]()


### Advanced Handcrafted Indicators

\[79\] W. Meng, X. Chen, W. Cui, and
J. Guo, "Wihgr: A robust wifi-based human gesture recognition system via
sparse recovery and modified attention-based bgru,"IoT-J, vol. 9, no.
12, pp. 10 272--10 282, 2021. [paper]()

\[80\] J. Huang, B. Liu, C. Miao, Y . Lu, Q. Zheng, Y . Wu, J. Liu, L.
Su, and C. W. Chen, "Phaseanti: An anti-interference wifi-based activity
recognition system using interference-independent phase component," IEEE
TMC, vol. 22, no. 5, pp. 2938--2954, 2021. [paper]()

\[81\] R. Gao, W. Li, Y . Xie, E. Yi, L. Wang, D. Wu, and D. Zhang,
"Towards robust gesture recognition by characterizing the sensing
quality of wifi signals,"IMWUT, vol. 6, no. 1, pp. 1--26, 2022. [paper]()

\[82\] J. Zhang, Y . Li, H. Xiong, D. Dou, C. Miao, and D. Zhang,
"Handgest: Hierarchical sensing for robust-in-the-air handwriting
recognition with commodity wifi devices,"IoT-J, vol. 9, no. 19, pp. 19
529--19 544, 2022. [paper]()

\[83\] X. Yu, T. Jiang, X. Ding, Z. Yao, X. Zhou, and Y . Zhong,
"Towards position-independent gesture recognition based on wifi by
subcarrier selection and gesture code," inWCNC. IEEE, 2023, pp. 1--6. [paper]()

\[84\] Y . Zhang, Q. Liu, Y . Wang, and G. Yu, "Csi-based
location-independent human activity recognition using feature
fusion,"IEEE TIM, vol. 71, pp. 1--12, 2022. [paper]()

\[85\] C. Peng, L. Gui, B. Sheng, Z. Guo, and F. Xiao, "Rosefi: A robust
sedentary behavior monitoring system with commodity wifi devices," IEEE
TMC, 2023. [paper]()

\[86\] X. Wang, A. Yu, K. Niu, W. Shi, J. Wang, Z. Yao, R. C. Shah, H.
Lu, and D. Zhang, "Understanding the diffraction model in static
multipath- rich environments for wifi sensing system design,"IEEE TMC,
2024. [paper]()

\[87\] X. Ding, X. Yu, Y . Zhong, W. Xie, B. Cai, M. You, and T. Jiang,
"Robust gesture recognition method toward intelligent environment using
wi-fi signals,"Measurement, vol. 231, p. 114525, 2024. [paper]()

\[88\] M. Peng, X. Fu, H. Zhao, Y . Wang, and C. Kai, "Likey: Location-
independent keystroke recognition on numeric keypads using wifi
signal,"Computer Networks, vol. 245, p. 110354, 2024. [paper]()

\[89\] Q. Bu, G. Yang, J. Feng, and X. Ming, "Wi-fi based gesture
recognition using deep transfer learning," inSmartWorld, Ubiquitous
Intelligence & Computing, Advanced & Trusted Computing, Scalable
Computing & Communications, Cloud & Big Data Computing, Internet of
People and Smart City Innovation. IEEE, 2018, pp. 590--595. [paper]()

\[90\] C. Zhang, W. Jiao, and W. Du, "Enhancing human activity
recognition performance in small-sample wi-fi sensing using data
augmentation methods," inICCT. IEEE, 2023, pp. 473--478. [paper]()

### Motion Indicators

\[91\] F. Meneghello, D. Garlisi, N. Dal Fabbro, I. Tinnirello, and M.
Rossi, "Sharp: Environment and person independent activity recognition
with commodity ieee 802.11 access points,"IEEE TMC, vol. 22, no. 10,
pp. 6160--6175, 2022. [paper]()

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240. [paper]()

\[93\] Y . Yin, Z. Zhang, X. Yang, F. Yan, and Q. Niu, "Towards fully
domain- independent gesture recognition using cots wifi
device,"Electronics Letters, vol. 57, no. 5, pp. 232--234, 2021. [paper]()

\[94\] C. Feng, N. Wang, Y . Jiang, X. Zheng, K. Li, Z. Wang, and X.
Chen, "Wi-learner: Towards one-shot learning for cross-domain wi-fi
based gesture recognition,"IMWUT, vol. 6, no. 3, pp. 1--27, 2022. [paper]()

\[95\] K. Niu, F. Zhang, X. Wang, Q. Lv, H. Luo, and D. Zhang, "Under-
standing wifi signal frequency features for position-independent gesture
sensing,"IEEE TMC, vol. 21, no. 11, pp. 4156--4171, 2021. [paper]()

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024. [paper]()

\[97\] S. Li, Z. Liu, Q. Lv, Y . Zou, Y . Zhang, and D. Zhang, "Wilife:
Long-term daily status monitoring and habit mining of the elderly
leveraging ubiquitous wi-fi signals,"ACM Transactions on Computing for
Healthcare. [paper]()

\[98\] B. van Berlo, C. Oerlemans, F. L. Marogna, T. Ozcelebi, and N.
Merat- nia, "Mini-batch alignment: A deep-learning model for domain
factor- independent feature extraction for wi-fi--csi data,"Sensors,
vol. 23, no. 23, p. 9534, 2023. [paper]()

\[99\] B. van Berlo, T. Ozcelebi, and N. Meratnia, "Insights on mini-
batch alignment for wifi-csi data domain factor independent feature
extraction," inInternational Conference on Pervasive Computing and
Communications Workshops and other Affiliated Event. IEEE, 2022,
pp. 527--532. [paper]()

\[69\] D. Wu, Y . Zeng, R. Gao, S. Li, Y . Li, R. C. Shah, H. Lu, and D.
Zhang, "Witraj: Robust indoor motion tracking with wifi signals,"IEEE
TMC, vol. 22, no. 5, pp. 3062--3078, 2021. [paper]()

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325. [paper]()

\[100\] B.-B. Zhang, D. Zhang, Y . Hu, and Y . Chen, "Unsupervised
domain adaptation for wifi gesture recognition," inWCNC. IEEE, 2023,
pp. 1--6. [paper]()

\[101\] M. Yang, H. Zhu, R. Zhu, F. Wu, L. Yin, and Y . Yang,
"Witransformer: A novel robust gesture recognition sensing model with
wifi,"Sensors, vol. 23, no. 5, p. 2612, 2023. [paper]()

\[102\] W. Shi, M. Duan, H. He, L. Lin, C. Yang, C. Li, and J. Zhao,
"Location adaptive motion recognition based on wi-fi feature
enhancement," Applied Sciences, vol. 13, no. 3, p. 1320, 2023. [paper]()

\[103\] I. Bulugu, "Gesture recognition system based on cross-domain csi
extracted from wi-fi devices combined with the 3d cnn,"Signal, Image and
Video Processing, vol. 17, no. 6, pp. 3201--3209, 2023. [paper]()

\[30\] Y . Zhang, Y . Zheng, G. Zhang, K. Qian, C. Qian, and Z. Yang,
"Gaitid: Robust wi-fi based gait recognition," inWASA. Springer, 2020,
pp. 730--742. [paper]()

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219. [paper]()

\[104\] G. Chi, G. Zhang, X. Ding, Q. Ma, Z. Yang, Z. Du, H. Xiao, and
Z. Liu, "Xfall: Domain adaptive wi-fi-based fall detection with cross-
modal supervision,"IEEE JASAC, 2024. [paper]()

\[105\] R. Gao, M. Zhang, J. Zhang, Y . Li, E. Yi, D. Wu, L. Wang, and
D. Zhang, "Towards position-independent sensing for gesture recogni-
tion with wi-fi,"IMWUT, vol. 5, no. 2, pp. 1--28, 2021. [paper]()

\[106\] C. Shi, J. Liu, N. Borodinov, B. Leao, and Y . Chen, "Towards
environment-independent behavior-based user authentication using wifi,"
inMASS. IEEE, 2020, pp. 666--674. [paper]()

\[107\] Y . Wang, Y . Tian, and R. Peng, "Position and orientation
independent wireless gesture recognition," inWCSP. IEEE, 2022,
pp. 466--471. [paper]()

\[108\] D. Wu, D. Zhang, C. Xu, Y . Wang, and H. Wang, "Widir: Walking
direction estimation using wireless signals," inUBICOMP, 2016,
pp. 351--362. [paper]()

\[109\] H. Wang, D. Zhang, J. Ma, Y . Wang, Y . Wang, D. Wu, T. Gu, and
B. Xie, "Human respiration detection with commodity wifi devices: Do
user location and body orientation matter?" inUBICOMP, 2016, pp. 25--36. [paper]()

\[63\] Y . Qin, S. Sigg, S. Pan, and Z. Li, "Direction-agnostic gesture
recog- nition system using commercial wifi devices,"Computer Communica-
tions, vol. 216, pp. 34--44, 2024. [paper]()

\[110\] L. Zhang, C. Wang, M. Ma, and D. Zhang, "Widigr: Direction-
independent gait recognition system using commercial wi-fi devices,"
IoT-J, vol. 7, no. 2, pp. 1178--1191, 2019. [paper]()

\[111\] L. Zhang, C. Wang, and D. Zhang, "Wi-pigr: Path independent gait
recognition with commodity wi-fi,"IEEE TMC, vol. 21, no. 9,
pp. 3414--3427, 2021. [paper]()

\[112\] F. Zhang, C. Wu, B. Wang, H.-Q. Lai, Y . Han, and K. R. Liu,
"Widetect: Robust motion detection with a statistical electromagnetic
model," IMWUT, vol. 3, no. 3, pp. 1--24, 2019. [paper]()

\[113\] G. Zhu, B. Wang, W. Gao, Y . Hu, C. Wu, and K. R. Liu,
"Wifi-based robust human and non-human motion recognition with deep
learning," inPerCom Workshops. IEEE, 2024, pp. 769--774. [paper]()

### Angle Indicators

\[114\] Y . Li, T. Jiang, X. Ding, and Y . Wang, "Location-free csi
based activity recognition with angle difference of arrival," inWCNC.
IEEE, 2020, pp. 1--6. [paper]()

\[115\] Z. Han, Z. Lu, Z. Hu, Y . Chen, and X. Wen, "On
position-independency passive gesture tracking with commodity
wi-fi,"IEEE Sensors Journal, vol. 23, no. 14, pp. 16 264--16 275, 2023. [paper]()

\[116\] Y . Ren and J. Yang, "Robust person identification: A wifi
vision-based approach,"arXiv preprint arXiv:2210.00127, 2022. [paper]()


> ### **Key Takeaways and Lessons Learned: Signal Preprocessing**
>
> - **Signal Analysis for Denoising:**  
>   Algorithms like LRSD, SSA, and PCA are fundamental for extracting action-related components from background noise. These methods enhance resilience to location variations and enable robust monitoring (e.g., breath detection) even in non-ideal positions.
>
> - **Handcrafted IQ & Phase Features:**  
>   Advanced indicators derived from phase differences or the IQ complex plane (e.g., SPD, rotational features) capture fine-grained patterns. Notably, features like NLPEV provide independence from CCI, which is crucial for real-world robustness.
>
> - **Physical Invariance via Motion Indicators:**  
>   Transitioning to speed/velocity profiles, particularly the BVP and the Fresnel Zone Model, represents a major shift toward domain invariance. By mapping signals to speed or body-relative coordinates, systems decouple sensing from the user's orientation and environment.
>
> - **Geometric Consistency with Angle Indicators:**  
>   Angle-based measurements, such as AoA and ADoA, provide spatial geometric paths that remain consistent across domains. These allow for real-time trajectory reconstruction and 3D body representation, enabling complex tasks like person re-identification.
>
> - **Signal-to-Visual Feature Enrichment:**  
>   Converting 1D CSI time-series into 2D representations (e.g., Recurrence Plots, Grayscale images) bridges the gap between signal processing and computer vision, allowing models to benefit from powerful pre-trained visual architectures and data augmentation.



## Stage 3: 🦊 Feature Learning
<br>

Table IV: Comparison of Pros, Cons, and Best-fit Scenarios of Feature Learning Techniques in Wi-Fi Sensing.
| Category | Pros (Advantages) | Cons (Limitations) | Generalization Mechanism | Best-fit Scenarios |
|-----------|------------------|--------------------|---------------------------|--------------------|
| **Domain Alignment** <br>(Wang et al., 2021; Sheng et al., 2023; Zhang et al., 2021; Zhou et al., 2024; Zou et al., 2018; Li et al., 2021; Zhang et al., 2021; Jiang et al., 2018; Khattak et al., 2022; Wang et al., 2019; Zhang et al., 2024; Zinys et al., 2021; Strohmayer et al., 2024; Liu et al., 2023; Yin et al., 2021; Yang et al., 2024; Qin et al., 2023; Berlo et al., 2023; Zhou et al.; Yan et al., 2024; Li et al., 2021; Shi et al., 2020; Chen et al., 2022; Gretton et al., 2006; Zhou et al., 2024; Rao et al., 2024; Kang et al., 2021; Liang et al., 2023; Zhang et al., 2023; Mehryar et al., 2023; Zhou et al., 2020; Xiao et al., 2024; Kang et al., 2019; Jiao et al., 2024; Gong et al., 2024; Sheng et al., 2024; Chen et al.; Zhan et al., 2024; Wang et al., 2022; Ding et al., 2020; Zhang et al., 2022; Zhang et al., 2022; Mao et al., 2024; Xiao et al., 2023; Zhang et al., 2018; Sugimoto et al., 2023; Zhang et al., 2023; Islam et al., 2020; Wang et al., 2024) | Mitigates domain and hardware shifts; statistical metrics provide theoretical grounding. | Risk of suppressing discriminative motion features during aggressive alignment. | Enforces distribution-level invariance by aligning feature statistics across domains (e.g., adversarial learning, MMD). | Large domain shifts (e.g., cross-room or cross-device) with labeled source and unlabeled target data. |
| **Disentanglement** <br>(Elujide et al., 2022; Chen et al., 2024; Wang et al., 2019; Hao et al., 2021; Wu et al., 2021) | Strong physical interpretability; separates motion features from environment or identity noise. | Requires complex architectures (e.g., GANs or autoencoders) and careful hyperparameter tuning. | Factorizes latent representations into independent components to isolate task-relevant signals. | Scenarios with multiple interference factors (e.g., identical gestures by different users or locations). |
| **Metric Learning** <br>(Zhou et al., 2022; Wei et al., 2024; Bu et al., 2022; Liu et al., 2024; Zhang et al., 2024; Wu et al., 2018; Xiao et al., 2022; Xu et al., 2022; Wang et al., 2024; Xiao et al., 2024; Ren et al., 2022; Liang et al., 2024; Zhao et al., 2024; Wang et al., 2020; Hu et al., 2021; Zhang et al., 2023; Zhang et al., 2022; Shi et al., 2022; Shi et al., 2020; Shi et al., 2020; Zhao et al., 2024; Ding et al., 2021; Bahadori et al., 2022; Ding et al., 2021; Gu et al., 2021; Wang et al., 2022; Yang et al., 2023; Zhang et al., 2021) | Native few-shot and zero-shot support; scalable to new classes via template updates. | Highly dependent on support set quality; risk of class overlap in the embedding space. | Structures the embedding space by minimizing intra-class distance and maximizing inter-class separability. | Scenarios with extreme scarcity of target labels or dynamic needs for novel class recognition. |
| **Meta Learning** <br>(Huang et al., 2022; Zhou et al., 2022; Gao et al., 2023; Sheng et al., 2024; Zhao et al., 2024; Feng et al., 2022; Ding et al., 2020; Gao et al., 2022; Zhang et al., 2022; Zhang et al., 2020) | Rapid adaptation to new tasks; learns an initialization for fast convergence. | High computational cost during offline meta-training (e.g., second-order gradients). | Optimizes model parameters for fast task-level adaptation through episodic training across domains. | Edge deployment requiring immediate high accuracy after minimal user calibration. |
| **Data Synthesis** <br>(Li et al., 2021; Wang et al., 2020; Zhang et al., 2023; Huang et al., 2024; Wang et al., 2021; Zhang et al., 2023; Zhang et al., 2024; Xiao et al., 2019; Chen et al., 2022; Chen et al., 2020; Yan et al., 2024; Xiao et al., 2024; Zhou et al., 2022; Wang et al., 2018; Lan et al., 2024; Zhou et al., 2022; Wang et al., 2022; Hou et al., 2024; Liu et al., 2023; Virmani et al., 2017; Mao et al., 2024; Wang et al., 2025; Xiao et al., 2022; Xiao et al., 2021; Zhao et al., 2024; Wang et al., 2024) | Directly mitigates data scarcity; generative models improve coverage of rare cases. | Potential sim-to-real gap between synthetic samples and real-world signal data. | Expands training distributions by synthesizing diverse or unseen signal patterns. | Plug-in augmentation for tasks with insufficient, imbalanced, or hard-to-collect labeled data. |
| **Pseudo Labeling** <br>(Zhou et al., 2022; Chen et al.; Zhang et al., 2023; Sheng et al., 2023; Zhang et al., 2023) | Leverages abundant unlabeled target data via self-training. | Risk of error accumulation from early incorrect pseudo-labels. | Iteratively refines decision boundaries using confident predictions as surrogate labels. | Semi-supervised sensing tasks with long-term accumulation of unlabeled data. |

### Domain Alignment

#### Domain Alignment with Domain Discriminator

![fig7](https://github.com/user-attachments/assets/e65d5d71-4242-4899-a5f7-c99dd335bcb3)

Fig 7: Domain alignment with domain discriminator or domain classifier. Both source and target data are mapped into a shared feature space. Through adversarial competition between an action classifier and a domain discriminator, the network learns to produce domain-agnostic representations that enhance cross-domain performance.


\[117\] Z. Wang, S. Chen, W. Yang, and Y . Xu, "Environment-independent
wi-fi human activity recognition with adversarial network," inICASSP.
IEEE, 2021, pp. 3330--3334. [paper]()

\[118\] L. Sheng, Y . Chen, S. Ning, S. Wang, B. Lian, and Z. Wei, "Da-
har: Dual adversarial network for environment-independent wifi human
activity recognition,"Pervasive and Mobile Computing, vol. 96,
p. 101850, 2023. [paper]()

\[119\] L. Zhang, W. Cui, B. Li, Z. Chen, M. Wu, and T. S. Gee,
"Privacy- preserving cross-environment human activity recognition,"IEEE
Trans- actions on Cybernetics, vol. 53, no. 3, pp. 1765--1775, 2021. [paper]()

\[120\] Z. Zhou, F. Wang, and W. Gong, "i-sample: Augment domain adver-
sarial adaptation models for wifi-based har,"ACM ToSN, vol. 20, no. 2,
pp. 1--20, 2024. [paper]()

\[121\] H. Zou, J. Yang, Y . Zhou, and C. J. Spanos, "Joint adversarial
domain adaptation for resilient wifi-enabled device-free gesture
recognition," inICMLA. IEEE, 2018, pp. 202--207. [paper]()

\[122\] X. Li, L. Chang, F. Song, J. Wang, X. Chen, Z. Tang, and Z.
Wang, "Crossgr: Accurate and low-cost cross-target gesture recognition
using wi-fi,"IMWUT, vol. 5, no. 1, pp. 1--23, 2021. [paper]()

\[123\] H. Zhang, Z. Zhou, and W. Gong, "Wi-adaptor: Fine-grained domain
adaptation in wifi-based activity recognition," inGLOBECOM. IEEE, 2021,
pp. 1--6. [paper]()


#### Domain Alignment with Domain Classifier



\[124\] W. Jiang, C. Miao, F. Ma, S. Yao, Y . Wang, Y . Yuan, H. Xue, C.
Song, X. Ma, D. Koutsonikolas, W. Xu, and L. Su, "Towards environment
independent device free human activity recognition," inMobiCom, 2018,
pp. 289--304. [paper]()

\[125\] A. Khattak and A. Khan, "Cross-location activity recognition
using adversarial learning," inSOICT, 2022, pp. 59--65. [paper]()

\[126\] F. Wang, J. Liu, and W. Gong, "Wicar: Wifi-based in-car activity
recog- nition with multi-adversarial domain adaptation," inIWQoS, 2019,
pp. 1--10.\[127\] X. Zhang, Y . Feng, J. Huang, H. Yan, P. Zhao, J. Liu,
T. Liu, M. Li, Z. Liu, and B. Liu, "Objective gesture recognition based
on wifi," Authorea Preprints, 2024. [paper]()

\[128\] A. Zinys, B. van Berlo, and N. Meratnia, "A domain-independent
generative adversarial network for activity recognition using wifi csi
data,"Sensors, vol. 21, no. 23, p. 7852, 2021. [paper]()

\[129\] J. Strohmayer, R. Sterzinger, M. W ¨odlinger, and M. Kampel,
"Datta: Domain-adversarial test-time adaptation for cross-domain
wifi-based human activity recognition,"arXiv preprint arXiv:2411.13284,
2024. [paper]()

\[130\] S. Liu, Z. Chen, M. Wu, C. Liu, and L. Chen, "Wisr: Wireless
domain generalization based on style randomization,"IEEE TMC, 2023. [paper]()

\[93\] Y . Yin, Z. Zhang, X. Yang, F. Yan, and Q. Niu, "Towards fully
domain- independent gesture recognition using cots wifi
device,"Electronics Letters, vol. 57, no. 5, pp. 232--234, 2021. [paper]()

\[131\] W. Yang, X. Jiawei, W. Ao, X. Huijuan, Z. Chuanxin, and J. Yimu,
"Domain-generalization human activity recognition model based on csi
instance normalization."Journal on Communication/Tongxin Xuebao,
vol. 45, no. 6, 2024. [paper]()

\[64\] Y . Qin, S. Pan, and Z. Li, "Cross-domain extendable gesture
recognition system using wifi signals,"Electronics Letters, vol. 59, no.
16, p. e12931, 2023. [paper]()

\[132\] B. v. Berlo, R. Verhoeven, and N. Meratnia, "Use of domain
labels dur- ing pre-training for domain-independent wifi-csi gesture
recognition," Sensors, vol. 23, no. 22, p. 9233, 2023. [paper]()

\[133\] S. Zhou, L. Guo, Z. Lu, X. Wen, W. Zheng, and Y . Wang,
"Subject- independent human pose image construction with commodity
wi-fi," inIEEE ICC, 2021, pp. 1--6. [paper]()

\[134\] D. Yan, P. Yang, F. Shang, F. Han, Y . Yan, and X.-Y . Li,
"freegait: Liberalizing wireless-based gait recognition to mitigate
non-gait human behaviors," inMobiHoc, 2024, pp. 241--250. [paper]()

\[135\] H. Li, X. Chen, J. Wang, D. Wu, and X. Liu, "Dafi: Wifi-based
device- free indoor localization via domain adaptation,"IMWUT, vol. 5,
no. 4, pp. 1--21, 2021. [paper]()

\[106\] C. Shi, J. Liu, N. Borodinov, B. Leao, and Y . Chen, "Towards
environment-independent behavior-based user authentication using wifi,"
inMASS. IEEE, 2020, pp. 666--674. [paper]()

\[136\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fidora:
Robust wifi-based indoor localization via unsupervised domain
adaptation," IoT-J, vol. 9, no. 12, pp. 9872--9888, 2022. [paper]()


#### Domain Alignment with Similarity Computing
<img width="985" height="438" alt="fig8" src="https://github.com/user-attachments/assets/9c5dfa39-92a3-4afc-be25-28eaceddf517" />

Fig 8: Maximum Mean Discrepancy (MMD) quantifies the similarity between two probability distributions by projecting data into a Reproducing Kernel Hilbert Space (RKHS) and computing the squared distance between their mean embeddings, encouraging the model to learn domain-invariant representations.


\[137\] A. Gretton, K. Borgwardt, M. Rasch, B. Sch ¨olkopf, and A.
Smola, "A kernel method for the two-sample-problem,"NeurIPS, vol. 19,
2006. [paper]()

\[138\] Y . Zhou, J. Yang, H. Huang, and L. Xie, "Adapose: Towards
cross-site device-free human pose estimation with commodity wifi,"IoT-J,
2024. [paper]()

\[139\] X. Rao, L. Qin, Y . Yi, J. Liu, G. Lei, and Y . Cao, "A novel
adaptive device-free passive indoor fingerprinting localization under
dynamic environment,"IEEE TNSM, 2024. [paper]()

\[140\] H. Kang, Q. Zhang, and Q. Huang, "Context-aware wireless-based
cross-domain gesture recognition,"IoT-J, vol. 8, no. 17, pp. 13 503-- 13
515, 2021. [paper]()

\[141\] Y . Liang, W. Wu, H. Li, F. Han, Z. Liu, P. Xu, X. Lian, and X.
Chen, "Wiai-id: Wi-fi-based domain adaptation for appearance-independent
passive person identification,"IoT-J, vol. 11, no. 1, pp. 1012--1027,
2023. [paper]()

\[142\] S. Zhang, T. Jiang, X. Ding, X. Zhou, and Y . Zhong,
"Device-free cross-environment human action recognition using wi-fi
signals," in International Conference on Artificial Intelligence in
China. Springer, 2023, pp. 141--151. [paper]()

\[143\] S. Mehryar, "A domain adaptation framework for human activity
monitoring using passive wi-fi sensing," inICCCMLA. IEEE, 2023,
pp. 263--268. [paper]()

\[144\] R. Zhou, H. Hou, Z. Gong, Z. Chen, K. Tang, and B. Zhou,
"Adaptive device-free localization in dynamic environments through
adaptive neural networks,"IEEE Sensors Journal, vol. 21, no. 1,
pp. 548--559, 2020. [paper]()

\[145\] Z. Xiao, S. Zhou, X. Wen, S. Ling, and X. Yang,
"Pattern-independent human gait identification with commodity wifi,"
inWCNC. IEEE, 2024, pp. 1--6. [paper]()

\[146\] G. Kang, L. Jiang, Y . Yang, and A. G. Hauptmann, "Contrastive
adaptation network for unsupervised domain adaptation," inCVPR, 2019,
pp. 4893--4902. [paper]()

\[147\] W. Cui, K. Wu, M. Wu, X. Li, and Z. Chen, "Wicau: Comprehen-
sive partial adaptation with uncertainty-aware for wifi-based cross-
environment activity recognition,"IEEE TIM, vol. 73, pp. 1--10, 2024. [paper]()

\[148\] W. Jiao, C. Zhang, W. Du, and S. Ma, "Wisda: Subdomain
adaptation human activity recognition method using wi-fi signals,"IEEE
TMC, 2024. [paper]()

\[149\] K. Gong, Y . Gao, and W. Dong, "Privacy-preserving and cross-
domain human sensing by federated domain adaptation with semantic
knowledge correction,"IMWUT, vol. 8, no. 1, pp. 1--26, 2024. [paper]()

\[150\] B. Sheng, R. Han, H. Cai, F. Xiao, L. Gui, and Z. Guo, "Cdfi:
Cross- domain action recognition using wifi signals,"IEEE TMC, 2024. [paper]()

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024. [paper]()

\[151\] X. Zhan and Z. Wu, "Indoor positioning based on channel state
information and deep learning domain adaptation," inICCAID, vol. 13105.
SPIE, 2024, pp. 918--930. [paper]()

\[152\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Airfi: empowering
wifi-based passive human gesture recognition to unseen environment via
domain generalization,"IEEE TMC, vol. 23, no. 2, pp. 1156--1168, 2022. [paper]()

\[153\] X. Ding, T. Jiang, Y . Li, W. Xue, and Y . Zhong, "Device-free
location- independent human activity recognition using transfer learning
based on cnn," inICC Workshops. IEEE, 2020, pp. 1--6. [paper]()

#### Domain Alignment with Generative Adversarial Networks
![fig9](https://github.com/user-attachments/assets/b0168d62-9452-4713-8d24-943fb51cb3a0)

Fig 9: Generative Adversarial Networks. Generator (G): The network responsible for creating synthetic data. Its primary objective is to learn the underlying distribution of the real data and produce samples that are indistinguishable from the ground truth to fool the discriminator. Discriminator (D): The network acting as a binary classifier. Its role is to evaluate both real data (x) and synthetic data (G(z)), outputting a probability that a given sample is real (from the actual dataset) rather than fake (produced by the generator). It provides the gradient signal that guides the generator to improve its realism.


\[154\] J. Zhang, Z. Chen, C. Luo, B. Wei, S. S. Kanhere, and J. Li,
"Metaganfi: Cross-domain unseen individual identification using wifi
signals,"IMWUT, vol. 6, no. 3, pp. 1--21, 2022. [paper]()

\[155\] H. Zhang, X. Chen, and S. Chen, "Cross-domain wi-fi sign
language recognition with gans," inICCBN, 2022, pp. 60--65. [paper]()

\[156\] Y . Mao, Z. Guo, B. Sheng, L. Gui, and F. Xiao, "Wi-cro:
Wifi-based cross domain activity recognition via modified gan,"IEEE TVT,
2024. [paper]()

\[157\] C. Xiao, Y . Lei, C. Liu, and J. Wu, "Mean teacher-based
cross-domain activity recognition using wifi signals,"IoT-J, vol. 10,
no. 14, pp. 12 787--12 797, 2023. [paper]()

#### Domain Alignment with Multi-task Learning
\[158\] J. Zhang, Z. Tang, M. Li, D. Fang, P. Nurmi, and Z. Wang,
"Crosssense: Towards cross-site and large-scale wifi sensing,"
inMobiCom, 2018, pp. 305--320. [paper]()

\[159\] Y . Sugimoto, H. Rizk, A. Uchiyama, and H. Yamaguchi, "Towards
environment-independent activity recognition using wi-fi csi with an
encoder-decoder network," inBodySys, 2023, pp. 13--18. [paper]()

\[160\] Y . Zhang, A. Cheng, B. Chen, Y . Wang, and L. Jia, "A location-
independent human activity recognition method based on csi: System,
architecture, implementation,"IEEE TMC, 2023. [paper]()

#### Domain Alignment with Cross-modal Embedding
\[161\] M. T. Islam and S. Nirjon, "Wi-fringe: Leveraging text semantics
in wifi csi-based device-free named gesture recognition," inDCOSS. IEEE,
2020, pp. 35--42. [paper]()

\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024. [paper]()

\[162\] H. Zhang, Y . Ren, H. Yuan, J. Zhang, and Y . Shen, "Wi-chat:
Large lan- guage model powered wi-fi sensing,"arXiv preprint
arXiv:2502.12421, 2025. [paper]()

\[163\] I. Nirmal, A. Khamis, M. Hassan, W. Hu, R. Li, and A.
Kalyanaraman, "Wifi2radar: Orientation-independent single-receiver wifi
sensing via wifi to radar translation,"IoT-J, vol. 11, no. 9, pp. 15
750--15 766, 2024. [paper]()


### Component Disentangle
\[164\] I. Elujide, C. Feng, A. Shiran, J. Li, and Y . Liu, "Location
indepen- dent gesture recognition using channel state information,"
inAnnual Consumer Communications & Networking Conference. IEEE, 2022,
pp. 841--846. [paper]()

\[165\] Y .-J. Chen, W. Chen, S. Q. Zhang, H.-Y . Huang, and H. Kung, "A
task- oriented deep learning approach for human localization,"IEEE TCDS,
2024. [paper]()

\[45\] F. Wang, S. Zhou, S. Panev, J. Han, and D. Huang,
"Person-in-wifi: Fine-grained person perception using wifi," inICCV,
2019, pp. 5452-- 5461. [paper]()

\[166\] Z. Hao, J. Niu, X.-c. Dang, and Z. Qiao, "Wi-piga: A personnel-
independentmethod for actions recognition based on wi-fi," inBigCom.
IEEE, 2021, pp. 52--59. [paper]()

\[167\] B. Wu, T. Jiang, J. Yu, X. Ding, S. Wu, and Y . Zhong,
"Device-free human activity recognition with identity-based transfer
mechanism," in WCNC. IEEE, 2021, pp. 1--6. [paper]()


### Metric Learning for Zero/Few-shot Learning

#### Metric Learning with Triplet Loss

<img width="984" height="424" alt="fig10" src="https://github.com/user-attachments/assets/e0e28a5d-daee-4c79-98fb-f3926da52d35" />

Fig 10: Triplet loss aims to structure the feature space such that samples from the same class are mapped close together ($x_1^+, x_2^+$), while samples from different classes are pushed farther apart ($x^+, x^-$).



\[167\] B. Wu, T. Jiang, J. Yu, X. Ding, S. Wu, and Y . Zhong,
"Device-free human activity recognition with identity-based transfer
mechanism," in WCNC. IEEE, 2021, pp. 1--6. [paper]()

\[168\] Q. Zhou, Q. Yang, and J. Xing, "Enabling efficient wifi-based
occupant behavior recognition using insufficient samples,"Building and
Environ- ment, vol. 212, p. 108806, 2022. [paper]()

\[169\] Z. Wei, W. Chen, W. Tao, S. Ning, B. Lian, X. Sun, and J. Zhao,
"Catfsid: A few-shot human identification system based on cross- domain
adversarial training,"Computer Communications, vol. 224, pp. 275--284,
2024. [paper]()

\[170\] Q. Bu, X. Ming, J. Hu, T. Zhang, J. Feng, and J. Zhang,
"Transfersense: towards environment independent and one-shot wifi
sensing,"Personal and Ubiquitous Computing, pp. 1--19, 2022. [paper]()

\[171\] Y . Liu, A. Yu, L. Wang, B. Guo, Y . Li, E. Yi, and D. Zhang,
"Unifi: A unified framework for generalizable gesture recognition with
wi-fi signals using consistency-guided multi-view networks,"IMWUT,
vol. 7, no. 4, pp. 1--29, 2024. [paper]()

\[172\] X. Zhang, J. Huang, H. Yan, P. Zhao, G. Zhuang, Z. Liu, and B.
Liu, "Wiopen: A robust wi-fi-based open-set gesture recognition
framework,"arXiv preprint arXiv:2402.00822, 2024. [paper]()

\[173\] Z. Wu, A. A. Efros, and S. X. Yu, "Improving generalization via
scalable neighborhood component analysis," inECCV, 2018, pp. 685-- 701. [paper]()

\[174\] C. Xiao, S. Chen, F. Zhou, and J. Wu, "Self-supervised few-shot
time-series segmentation for activity recognition,"IEEE TMC, vol. 22,
no. 11, pp. 6770--6783, 2022. [paper]()

#### Learning with Contrastive Learning
\[175\] K. Xu, J. Wang, L. Zhang, H. Zhu, and D. Zheng, "Dual-stream
contrastive learning for channel state information based human activity
recognition,"JBHI, vol. 27, no. 1, pp. 329--338, 2022. [paper]()

\[176\] Y . Wang, G. Yu, Y . Zhang, D. Liu, and Y . Zhang, "Csi-based
location- independent human activity recognition by contrast between
dual stream fusion features,"IEEE Sensors Journal, 2024. [paper]()

\[177\] C. Xiao,
Y . Han, W. Yang, Y . Hou, F. Shi, and K. Chetty, "Diffusion model-based
contrastive learning for human activity recognition,"IoT- J, 2024. [paper]()

#### Metric Learning with Siamese Neural Networks
<img width="1020" height="526" alt="image" src="https://github.com/user-attachments/assets/7d6f4e5b-27e9-43b9-99a0-ea41cdae5b2d" />

Fig 11: Siamese Neural Networks. (1) The network takes a pair of inputs (e.g., two CSI segments) and feeds them into two identical sub-networks. Both branches share the same parameters (weights), mapping the inputs into a common low-dimensional feature space. (2) The model computes a similarity metric (usually Euclidean distance or Cosine similarity) between the two generated feature vectors. (3) Based on the distance, the system determines whether the two inputs belong to the same class (small distance) or different classes (large distance), often using a contrastive loss function.

\[116\] Y . Ren and J. Yang, "Robust person identification: A wifi
vision-based approach,"arXiv preprint arXiv:2210.00127, 2022. [paper]()

\[178\] Y . Liang, H. Li, W. Wu, and P. Xu, "Map-sgan: Multi-anchor
point siamese gan for wi-fi csi-based cross-domain gait
recognition,"ESWA, vol. 251, p. 124083, 2024. [paper]()

\[179\] Z. Zhao, T. Chen, Z. Cai, X. Li, H. Li, Q. Chen, and G. Zhu,
"Crossfi: A cross domain wi-fi sensing framework based on siamese
network," arXiv preprint arXiv:2408.10919, 2024. [paper]()


#### Metric Learning with Relation Network

<img width="854" height="471" alt="image" src="https://github.com/user-attachments/assets/d45cc7a5-55dc-4908-84b3-6619e8b9b3a3" />

Fig 12: Relation Network. (1) Both the support set and the query sample are passed through an embedding backbone to extract their respective feature maps. (2)The query feature map is paired and concatenated with each feature map in the support set, creating combined feature representations. (3) These concatenated pairs are fed into a Relation Module (usually a non-linear CNN or MLP), which acts as a learnable metric to calculate a relation score (between 0 and 1) for each pair. (4) The query is assigned to the class with the highest relation score, representing the strongest similarity determined by the deep neural network rather than a fixed distance metric.

\[180\] J. Wang, Q. Gao, X. Ma, Y . Zhao, and Y . Fang, "Learning to
sense: Deep learning for wireless sensing with less training
efforts,"IEEE Wireless Communications, vol. 27, no. 3, pp. 156--162,
2020. [paper]()

\[181\] P. Hu, C. Tang, K. Yin, and X. Zhang, "Wigr: a practical wi-fi-
based gesture recognition system with a lightweight few-shot network,"
Applied Sciences, vol. 11, no. 8, p. 3329, 2021. [paper]()

\[182\] L. Zhang, S. Wu, T. Zhang, and Q. Zhang, "Learning to locate:
Adaptive fingerprint-based localization with few-shot relation learning
in dynamic indoor environments,"IEEE TWC, vol. 22, no. 8, pp. 5253--
5264, 2023. [paper]()

\[183\] R. Zhang, C. Jiang, S. Wu, Q. Zhou, X. Jing, and J. Mu, "Wi-fi
sensing for joint gesture recognition and human identification from few
samples in human-computer interaction,"IEEE JASAC, vol. 40, no. 7,
pp. 2193-- 2205, 2022. [paper]()

#### Metric Learning with Matching Network

![fig13](https://github.com/user-attachments/assets/ec3ee2c2-3185-43fd-a378-e8d8620c896b)

Fig 13: Matching Network. (1) Both the small support set and the query sample are mapped into a shared low-dimensional feature space using a neural network.
(2) The model computes the cosine similarity (or distance metric) between the query embedding and each embedding in the support set.
(3) These similarity scores are processed through a softmax function to generate attention weights, indicating which support examples most closely resemble the query.
(4) The final label is predicted by a weighted sum of the support set labels, allowing the model to recognize new classes without any parameter updates.

\[184\] Z. Shi, Q. Cheng, J. A. Zhang, and R. Y . Da Xu,
"Environment-robust wifi-based human activity recognition using enhanced
csi and deep learning,"IoT-J, vol. 9, no. 24, pp. 24 643--24 654, 2022. [paper]()

\[185\] Z. Shi, J. A. Zhang, R. Xu, Q. Cheng, and A. Pearce, "Towards
environment-independent human activity recognition using deep learn- ing
and enhanced csi," inIEEE GLOBECOM. IEEE, 2020, pp. 1--6. [paper]()

\[186\] Z. Shi, J. A. Zhang, R. Y . Xu, and Q. Cheng,
"Environment-robust device-free human activity recognition with
channel-state-information enhancement and one-shot learning,"IEEE TMC,
vol. 21, no. 2, pp. 540--554, 2020. [paper]()

\[188\] X. Ding, T. Jiang, Y . Zhong, Y . Huang, and Z. Li, "Wi-fi-based
location-independent human activity recognition via meta learning,"
Sensors, vol. 21, no. 8, p. 2654, 2021. [paper]()

#### Metric Learning with Prototypical Network

<img width="1001" height="560" alt="image" src="https://github.com/user-attachments/assets/40b2a8bb-a078-458b-bfb3-521c816159c2" />

Fig 14: Prototypical Network. (1) For each class in the support set, the model computes a prototype (mean vector) by averaging the feature embeddings of all samples belonging to that class. (2) The query sample is mapped into the same feature space using the shared embedding backbone. (3) The model calculates the Euclidean distance between the query embedding and each class prototype. (4) The query is classified based on a softmax distribution over the negative distances; it is assigned to the class whose prototype is nearest in the embedding space.


\[66\] N. Bahadori, J. Ashdown, and F. Restuccia, "Rewis: Reliable wi-fi
sensing through few-shot multi-antenna multi-receiver csi learning," in
WoWMoM. IEEE, 2022, pp. 50--59. [paper]()

\[189\] X. Ding, T. Jiang, Y . Zhong, J. Yang, Y . Huang, and Z. Li,
"Device-free location-independent human activity recognition via
few-shot learning," inIEEE/CIC ICC in China, 2021, pp. 106--111. [paper]()

\[190\] Y . Gu, H. Yan, M. Dong, M. Wang, X. Zhang, Z. Liu, and F. Ren,
"Wione: one-shot learning for environment-robust device-free user
authentication via commodity wi-fi in man--machine system,"IEEE
Transactions on Computational Social Systems, vol. 8, no. 3, pp. 630--
642, 2021. [paper]()

\[191\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Caution: A robust
wifi- based human authentication system via few-shot open-set
recognition," IoT-J, vol. 9, no. 18, pp. 17 323--17 333, 2022. [paper]()

\[192\] B. Yang, H. Wang, L. Hu, H. Zhu, C.-T. Lam, and K. Fang,
"Few-shot cross-domain based wifi sensing system for online learning in
iot," IEEE Sensors Journal, 2023. [paper]()

\[187\] T. Zhao, N. Wang, G. Cao, S. Mao, and X. Wang, "Functional data
analysis assisted cross-domain wi-fi sensing using few-shot learning,"
inIEEE ICC. IEEE, 2024, pp. 4780--4785. [paper]()

\[193\] X. Zhang, C. Tang, K. Yin, and Q. Ni, "Wifi-based cross-domain
gesture recognition via modified prototypical networks,"IoT-J, vol. 9,
no. 11, pp. 8584--8596, 2021. [paper]()

### Meta Learning for Few-shot Learning

<img width="1394" height="563" alt="image" src="https://github.com/user-attachments/assets/609053f7-446f-4fdb-b605-8b02998c5a0a" />

Fig 15: Model-Agnostic Meta-Learning (MAML) includes a meta-training stage and a meta-testing stage. The meta-training stage is designed to find a good initialization of model parameters such that the model can quickly adapt to new tasks with only a few gradient steps and a small amount of labeled data in the meta-testing stage.

\[194\] C. Finn, P. Abbeel, and S. Levine, "Model-agnostic meta-learning
for fast adaptation of deep networks," inICML. PMLR, 2017, pp. 1126--
1135. [paper]()

\[195\] S. Huang, Y . Chen, D. Wu, G. Yu, and Y . Zhang, "Few-shot
learning for human activity recognition based on csi," inCACML. IEEE,
2022, pp. 403--409. [paper]()

\[196\] Z. Zhou, F. Wang, J. Yu, J. Ren, Z. Wang, and W. Gong, "Target-
oriented semi-supervised domain adaptation for wifi-based har," in IEEE
INFOCOM. IEEE, 2022, pp. 420--429. [paper]()

\[197\] J. Gao, D. Wu, F. Yin, Q. Kong, L. Xu, and S. Cui, "Metaloc:
Learning to learn wireless localization,"IEEE JASAC, 2023. [paper]()

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240. [paper]()

\[94\] C. Feng, N. Wang, Y . Jiang, X. Zheng, K. Li, Z. Wang, and X.
Chen, "Wi-learner: Towards one-shot learning for cross-domain wi-fi
based gesture recognition,"IMWUT, vol. 6, no. 3, pp. 1--27, 2022. [paper]()

\[198\] B. Sheng, R. Han, F. Xiao, Z. Guo, and L. Gui, "Metaformer:
Domain- adaptive wifi sensing with only one labelled target
sample,"IMWUT, vol. 8, no. 1, pp. 1--27, 2024. [paper]()

\[199\] S. Ding, Z. Chen, T. Zheng, and J. Luo, "Rf-net: A unified meta-
learning framework for rf-enabled one-shot human activity recogni-
tion," inSenSys, 2020, pp. 517--530. [paper]()

\[154\] J. Zhang, Z. Chen, C. Luo, B. Wei, S. S. Kanhere, and J. Li,
"Metaganfi: Cross-domain unseen individual identification using wifi
signals,"IMWUT, vol. 6, no. 3, pp. 1--21, 2022. [paper]()

\[200\] Z. Gao, J. Xue, J. Zhang, and W. Xiao, "Ml-wigr: A
meta-learning- based approach for cross-domain device-free gesture
recognition,"Soft Computing, vol. 26, no. 13, pp. 6145--6155, 2022. [paper]()

### Data Augmentationand Data Synthesize
\[122\] X. Li, L. Chang, F. Song, J. Wang, X. Chen, Z. Tang, and Z.
Wang, "Crossgr: Accurate and low-cost cross-target gesture recognition
using wi-fi,"IMWUT, vol. 5, no. 1, pp. 1--23, 2021. [paper]()

\[180\] J. Wang, Q. Gao, X. Ma, Y . Zhao, and Y . Fang, "Learning to
sense: Deep learning for wireless sensing with less training
efforts,"IEEE Wireless Communications, vol. 27, no. 3, pp. 156--162,
2020. [paper]()

\[201\] Y . Zhang, X. Wang, Y . Wang, and H. Chen, "Human activity
recogni- tion across scenes and categories based on csi,"IEEE TMC, 2020. [paper]()

\[202\] J. Zhang, Y . Dai, J. Chen, C. Luo, B. Wei, V . C. Leung, and J.
Li, "Sida: Self-supervised imbalanced domain adaptation for sound
enhancement and cross-domain wifi sensing,"IMWUT, vol. 7, no. 3,
pp. 1--24, 2023. [paper]()

\[203\] T. Huang, S. Wang, and S. Li, "Low-cost and user independent
action recognition using wifi signals,"Available at SSRN 4160593. [paper]()

\[182\] L. Zhang, S. Wu, T. Zhang, and Q. Zhang, "Learning to locate:
Adaptive fingerprint-based localization with few-shot relation learning
in dynamic indoor environments,"IEEE TWC, vol. 22, no. 8, pp. 5253--
5264, 2023. [paper]()

\[204\] Y . Wang, L. Yao, Y . Wang, and Y . Zhang, "Robust csi-based
human activity recognition with augment few shot learning,"IEEE Sensors
Journal, vol. 21, no. 21, pp. 24 297--24 308, 2021. [paper]()

\[205\] L. Zhang, Y . Jiang, Y . Ma, S. Mao, W. Huang, Z. Yu, X. Zheng,
L. Shu, X. Fan, and G. Xu, "Toward robust and effective behavior based
user authentication with off-the-shelf wi-fi,"IEEE TIFS, 2024. [paper]()

\[136\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fidora:
Robust wifi-based indoor localization via unsupervised domain
adaptation," IoT-J, vol. 9, no. 12, pp. 9872--9888, 2022. [paper]()

\[206\] C. Xiao, D. Han, Y . Ma, and Z. Qin, "Csigan: Robust channel
state information-based activity recognition with gans,"IoT-J, vol. 6,
no. 6, pp. 10 191--10 204, 2019. [paper]()

\[207\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fido:
Ubiquitous fine-grained wifi-based localization for unlabelled users via
domain adaptation," inProceedings of The Web Conference, 2020,
pp. 23--33. [paper]()

\[134\] D. Yan, P. Yang, F. Shang, F. Han, Y . Yan, and X.-Y . Li,
"freegait: Liberalizing wireless-based gait recognition to mitigate
non-gait human behaviors," inMobiHoc, 2024, pp. 241--250. [paper]()

\[177\] C. Xiao,
Y . Han, W. Yang, Y . Hou, F. Shi, and K. Chetty, "Diffusion model-based
contrastive learning for human activity recognition,"IoT- J, 2024. [paper]()

\[208\] D. Yan, F. Shang, P. Yang, F. Han, Y . Yan, and X.-Y . Li,
"freeloc: Wireless-based cross-domain device-free fingerprints
localization to free user's motions,"IoT-J, vol. 11, no. 14, pp. 25
099--25 110, 2024. [paper]()

\[209\] B. Zhou, R. Zhou, Y . Luo, and Y . Cheng, "Towards cross domain
csi action recognition through one-shot bimodal domain adaptation," in
MobiQuitous. Springer, 2022, pp. 290--309. [paper]()

\[210\] F. Wang, J. Han, S. Zhang, X. He, and D. Huang, "Csi-net:
Unified human body characterization and pose recognition,"arXiv preprint
arXiv:1810.03064, 2018. [paper]()

\[211\] B. Lan, F. Wang, L. Xia, F. Nai, S. Nie, H. Ding, and J. Han,
"Bullydetect: Detecting school physical bullying with wi-fi and deep
wavelet transformer,"IoT-J, 2024. [paper]()

\[212\] H. He, X. Huan, J. Wang, Y . Luo, H. Hu, and J. An, "P3id: A
privacy- preserving person identification framework towards
multi-environments based on transfer learning,"IEEE TMC, pp. 1--16,
2024. [paper]()

\[213\] H. Liu, L. Xi, W. Wang, F. Zhang, and Z. J. Haas, "Openfi:
Open-set wifi human sensing via virtual embedding confidence-aware,"IEEE
TNSE, pp. 1--12, 2024. [paper]()

\[152\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Airfi: empowering
wifi-based passive human gesture recognition to unseen environment via
domain generalization,"IEEE TMC, vol. 23, no. 2, pp. 1156--1168, 2022. [paper]()

\[214\] T. DeVries and G. W. Taylor, "Improved regularization of
convolutional neural networks with cutout,"arXiv preprint
arXiv:1708.04552, 2017. [paper]()

\[215\] W. Hou and C. Wu, "Rfboost: Understanding and boosting deep wifi
sensing via physical data augmentation,"IMWUT, vol. 8, no. 2, pp. 1--26,
2024. [paper]()

\[216\] S. Liu, Z. Chen, M. Wu, H. Wang, B. Xing, and L. Chen,
"Generalizing wireless cross-multiple-factor gesture recognition to
unseen domains," IEEE TMC, 2023. [paper]()

\[156\] Y . Mao, Z. Guo, B. Sheng, L. Gui, and F. Xiao, "Wi-cro:
Wifi-based cross domain activity recognition via modified gan,"IEEE TVT,
2024. [paper]()

\[217\] A. Virmani and M. Shahzad, "Position and orientation agnostic
gesture recognition using wifi," inMobiSys, 2017, pp. 252--264. [paper]()

\[174\] C. Xiao, S. Chen, F. Zhou, and J. Wu, "Self-supervised few-shot
time-series segmentation for activity recognition,"IEEE TMC, vol. 22,
no. 11, pp. 6770--6783, 2022. [paper]()

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219. [paper]()

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240. [paper]()

\[218\] S. Wang, L. Wang, and W. Liu, "Feature decoupling and
regeneration towards wifi-based human activity recognition,"Pattern
Recognition, vol. 153, p. 110480, 2024. [paper]()


### Pseudo Labeling
\[75\] R. Zhou, Z. Gong, K. Tang, B. Zhou, and Y . Cheng, "Device-free
cross location activity recognition via semi-supervised deep
learning,"Neural Computing and Applications, vol. 34, no. 12, pp. 10
189--10 203, 2022. [paper]()

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024. [paper]()

\[219\] B.-B. Zhang, D. Zhang, Y . Li, Y . Hu, and Y . Chen,
"Unsupervised domain adaptation for rf-based gesture recognition,"IoT-J,
vol. 10, no. 23, pp. 21 026--21 038, 2023. [paper]()

\[118\] L. Sheng, Y . Chen, S. Ning, S. Wang, B. Lian, and Z. Wei, "Da-
har: Dual adversarial network for environment-independent wifi human
activity recognition,"Pervasive and Mobile Computing, vol. 96,
p. 101850, 2023. [paper]()

\[100\] B.-B. Zhang, D. Zhang, Y . Hu, and Y . Chen, "Unsupervised
domain adaptation for wifi gesture recognition," inWCNC. IEEE, 2023,
pp. 1--6. [paper]()


> ### **Key Takeaways and Lessons Learned: Feature Learning**
>
> - **Domain Alignment for Distribution Matching:**  
>   Minimizing domain divergence via adversarial discriminators or statistical metrics (e.g., MMD, EMD) is fundamental. A key lesson is using cross-modal embeddings (e.g., BERT, GPT-4o) as “semantic anchors” to bridge the gap between raw CSI and high-level human activities.
>
> - **Component Disentanglement for Interpretability:**  
>   Explicitly separating environment, identity, and motion components using GANs or specialized encoders ensures that the model ignores environmental noise. This disentangled latent space is critical for handling multi-factor variations in real-world settings.
>
> - **Metric Learning for Few-shot Scalability:**  
>   Structuring the feature space using triplet loss, contrastive learning, or prototypical networks allows for clustering similar actions. The major takeaway is the high scalability of similarity-based matching, which enables zero/few-shot recognition of novel classes without retraining the backbone.
>
> - **Meta-Learning for Rapid Adaptation:**  
>   Paradigms like MAML and Reptile focus on “learning how to learn” by optimizing for a superior parameter initialization. This ensures that the sensing system can converge to a site-specific optimum with minimal gradient steps (e.g., one-shot or few-shot).
>
> - **Data Synthesis as a Robustness Plug-in:**  
>   Beyond simple augmentations, generative models (GANs, VAEs, and Diffusion) are essential for simulating target-domain conditions. These modules mitigate the Sim-to-Real gap by expanding training diversity with physically plausible synthetic signals.
>
> - **Pseudo Labeling for Iterative Refinement:**  
>   Leveraging abundant unlabeled target data through virtual labels reduces annotation costs. The iterative refinement of these labels (e.g., via confidence thresholds or centroid-based reassignment) is vital for long-term performance improvement in unfamiliar domains.


## Stage 4: :monkey: Model Deployment

<img width="1575" height="463" alt="deployment" src="https://github.com/user-attachments/assets/fecc906c-5d9c-4030-833b-ce70d0fb1daa" />
Fig 16: Wi-Fi sensing generalization methods in the deployment stage. (a) Few-shot fine-tuning. In this approach, a Wi-Fi sensing network is first pre-trained on a large-scale dataset to learn general feature extraction capabilities. During deployment, the parameters of the backbone are kept frozen, while only the task head is fine-tuned using data from the target scenario. This strategy enables rapid deployment in new environments with minimal computational overhead. (b) Federated Learning. This method involves aggregating data from diverse scenarios for centralized training on the server side. By exposing the model to a sufficiently wide range of environments during the training phase, it learns to capture robust, cross-domain features. Consequently, the model can be deployed into target scenarios, achieving seamless zero-shot generalization.
(c) Continual Learning. To handle the continuous influx of new sensing tasks and environmental data, the model evolves through sequential training stages as new data arrives, allowing it to incrementally acquire knowledge from novel scenarios. This approach ensures the model remains adaptive to dynamic environmental changes while mitigating the risk of catastrophic forgetting.


<br>

Table V: Comparison of Model Deployment Strategies in Wi-Fi Sensing.
| Approach | Pros (Advantages) | Cons (Limitations) | Generalization Mechanism | Best-fit Scenarios |
|-----------|------------------|--------------------|---------------------------|--------------------|
| **Transfer Learning** <br>(Wang et al., 2024; Lan et al., 2024; Ding et al., 2020; Chen et al., 2021; Brinke et al., 2019; Fang et al., 2020; Yin et al., 2022; Zheng et al., 2023; Bi et al., 2024; Hou et al., 2022; Hou et al., 2022) | Fast deployment by leveraging pre-trained weights.<br>Resource efficient with minimal fine-tuning on edge devices. | Requires labeled target samples.<br>Performance degrades under large domain gaps. | Adapts shared representations by fine-tuning higher layers to capture environment- or user-specific patterns. | Rapid adaptation to a specific new environment, user, or novel sensing task. |
| **Federated Learning** <br>(Hernandez et al., 2021; Geng et al., 2023; Li et al., 2023; Qi et al., 2023; Zhang et al., 2023; Zhang et al., 2021; Zhang et al., 2023) | Preserves data privacy as raw CSI remains local.<br>Benefits from collaborative learning across clients. | Communication overhead from frequent model synchronization.<br>Latency in large-scale deployments. | Learns globally robust models by aggregating heterogeneous local updates from diverse environments. | Privacy-sensitive applications such as home security or multi-user collaborative sensing. |
| **Continual Learning** <br>(Yang et al., 2023; Bai et al., 2019; Soltanaghaei et al., 2020; Zhai et al., 2021; Fu et al., 2024; Zhang et al., 2025; Zhang et al., 2023) | Incrementally acquires new knowledge with local updates.<br>Communication efficient for long-term deployment. | Risk of catastrophic forgetting.<br>Potential inference or update latency on COTS devices. | Maintains generalization over time by balancing knowledge retention and adaptation to new data distributions. | Long-term deployments where environments, furniture layouts, or user behaviors evolve. |

### Transfer Learning
\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024. [paper]()

\[210\] F. Wang, J. Han, S. Zhang, X. He, and D. Huang, "Csi-net:
Unified human body characterization and pose recognition,"arXiv preprint
arXiv:1810.03064, 2018. [paper]()

\[153\] X. Ding, T. Jiang, Y . Li, W. Xue, and Y . Zhong, "Device-free
location- independent human activity recognition using transfer learning
based on cnn," inICC Workshops. IEEE, 2020, pp. 1--6. [paper]()

\[220\] Y .-S. Chen, Y .-C. Chang, and C.-Y . Li, "A semi-supervised
transfer learning with dynamic associate domain adaptation for human
activity recognition using wifi signals,"Sensors, vol. 21, no. 24,
p. 8475, 2021. [paper]()

\[221\] J. K. Brinke and N. Meratnia, "Scaling activity recognition
using channel state information through convolutional neural networks
and transfer learning," inProceedings of the International Workshop on
Challenges in Artificial Intelligence and Machine Learning for Internet
of Things, 2019, pp. 56--62. [paper]()

\[222\] Y . Fang, B. Sheng, H. Wang, and F. Xiao, "Witransfer: A
cross-scene transfer activity recognition system using wifi," inTURC,
2020, pp. 59--63. [paper]()

\[223\] G. Yin, J. Zhang, G. Shen, and Y . Chen, "Fewsense, towards a
scalable and cross-domain wi-fi sensing system using few-shot
learning,"IEEE TMC, vol. 23, no. 1, pp. 453--468, 2022. [paper]()

\[224\] L. Zheng, S. Bi, S. Wang, Z. Quan, X. Li, X. Lin, and H. Wang,
"Resmon: Domain-adaptive wireless respiration state monitoring via
few-shot bayesian deep learning,"IoT-J, vol. 10, no. 23, pp. 20 914-- 20
927, 2023. [paper]()

\[225\] S. Bi, X. Chen, L. Zheng, H. Hou, and X. Lin, "Roger: Few-shot
learning based robust gesture recognition with multi-modal wi-fi csi
measurements," inICMLCN. IEEE, 2024, pp. 517--522.\[226\] H. Hou, S. Bi,
L. Zheng, X. Lin, and Z. Quan, "Sample-efficient cross- domain wifi
indoor crowd counting via few-shot learning," inWOCC. IEEE, 2022,
pp. 132--137. [paper]()

\[227\] H. Hou, S. Bi, L. Zheng, X. Lin, Y . Wu, and Z. Quan,
"Dasecount: Domain-agnostic sample-efficient wireless indoor crowd
counting via few-shot learning,"IoT-J, vol. 10, no. 8, pp. 7038--7050,
2022. [paper]()

### Federated Learning
\[228\] S. M. Hernandez and E. Bulut, "Wifederated: Scalable wifi
sensing using edge-based federated learning,"IoT-J, vol. 9, no. 14,
pp. 12 628-- 12 640, 2021. [paper]()

\[229\] H. Geng, D. Deng, W. Zhang, P. Ji, and X. Wu, "Personalized
federated learning based on bidirectional knowledge distillation for
wifi gesture recognition,"Electronics, vol. 12, no. 24, p. 5016, 2023. [paper]()

\[230\] X. Li, F. Song, M. Luo, K. Li, L. Chang, X. Chen, and Z. Wang,
"Towards collaborative and cross-domain wi-fi sensing: A case study for
human activity recognition,"IEEE TMC, vol. 23, no. 2, pp. 1674-- 1688,
2023. [paper]()

\[231\] W. Qi, R. Zhang, J. Zhou, H. Zhang, Y . Xie, and X. Jing, "A
resource-efficient cross-domain sensing method for device-free gesture
recognition with federated transfer learning,"IEEE TGCN, vol. 7, no. 1,
pp. 393--400, 2023. [paper]()

\[232\] S. Zhang, T. Jiang, X. Ding, Y . Zhong, and H. Jia, "A
cloud-edge col- laborative framework for cross-environment human action
recognition based on wi-fi," inIEEE/CIC ICC in China, 2023, pp. 1--6. [paper]()

\[119\] L. Zhang, W. Cui, B. Li, Z. Chen, M. Wu, and T. S. Gee,
"Privacy- preserving cross-environment human activity recognition,"IEEE
Trans- actions on Cybernetics, vol. 53, no. 3, pp. 1765--1775, 2021. [paper]()

\[233\] N. Zheng, Y . Li, S. Jiang, Y . Li, R. Yao, C. Dong, T. Chen, Y
. Yang, Z. Yin, and Y . Liu, "Adawifi, collaborative wifi sensing for
cross- environment adaptation,"IEEE TMC, pp. 1--15, 2024. [paper]()

\[234\] J. Zhang, Y . Li, Q. Li, and W. Xiao, "Variance-constrained
local--global modeling for device-free localization under
uncertainties,"IEEE TII, 2023. [paper]()



### Continual Learning
\[192\] B. Yang, H. Wang, L. Hu, H. Zhu, C.-T. Lam, and K. Fang,
"Few-shot cross-domain based wifi sensing system for online learning in
iot," IEEE Sensors Journal, 2023. [paper]()

\[235\] Y . Bai, Z. Wang, K. Zheng, X. Wang, and J. Wang, "Widrive:
Adaptive wifi-based recognition of driver activity for real-time and
safe takeover," inICDCS. IEEE, 2019, pp. 901--911. [paper]()

\[236\] E. Soltanaghaei, R. A. Sharma, Z. Wang, A. Chittilappilly, A.
Luong, E. Giler, K. Hall, S. Elias, and A. Rowe, "Robust and practical
wifi hu- man sensing using on-device learning with a domain adaptive
model," inProceedings of the ACM International Conference on Systems for
Energy-Efficient Buildings, Cities, and Transportation, 2020, pp. 150--
159. [paper]()

\[237\] S. Zhai, Z. Tang, P. Nurmi, D. Fang, X. Chen, and Z. Wang,
"Rise: Robust wireless sensing using probabilistic and statistical
assessments," inMobiCom, 2021, pp. 309--322. [paper]()

\[238\] Q. Fu, F. Wang, M. Zhu, H. Ding, J. Han, and T. X. Han, "Ccs:
Con- tinuous learning for customized incremental wireless sensing
services," arXiv preprint arXiv:2412.04821, 2024. [paper]()

\[239\] T. Zhang, Q. Fu, H. Ding, G. Wang, and F. Wang, "Carec:
Continual wireless action recognition with expansion-compression
coordination," Sensors, 2025. [paper]()

\[240\] Y . Zhang, F. He, Y . Wang, D. Wu, and G. Yu, "Csi-based cross-
scene human activity recognition with incremental learning,"Neural
Computing and Applications, vol. 35, no. 17, pp. 12 415--12 432, 2023. [paper]()

> ### **Key Takeaways and Lessons Learned: Model Deployment**
>
> - **Hierarchical Efficiency in Transfer Learning:**  
>   While fine-tuning the entire network yields superior accuracy, freezing the backbone and updating only the task head is most viable for resource-constrained edge devices. This strategy balances global feature representation with site-specific adaptation.
>
> - **Privacy-Preserving Collaborative Generalization:**  
>   Federated Learning is a powerful engine for building robust global models without moving raw CSI data. A major lesson is managing communication overhead during parameter exchange and addressing the performance drops caused by shifted data distributions across heterogeneous clients.
>
> - **Evolution through Continual Learning:**  
>   To handle long-term environmental drifts (e.g., furniture moving), models must incrementally acquire knowledge. The core challenge is mitigating catastrophic forgetting; strategies like data replay and dynamic model expansion are essential to preserve performance on original tasks.
>
> - **Minimizing User Burden in Online Adaptation:**  
>   Incorporating “User-in-the-loop” mechanisms allows for continuous refinement. The key takeaway is using anomaly detection and high-confidence sampling to minimize the labeling effort required from users during the adaptation phase.
>
> - **Systems-level Latency and Resource Trade-offs:**  
>   Beyond accuracy, real-world deployment on COTS chipsets requires balancing model update frequency with inference latency. For high-responsiveness applications, local updates must be optimized to prevent system bottlenecks.


---

##  🐱&🦩 Challenges and Future Directions 

### 🐬 Data, Data, Data

The scaling law, which involves training large-scale models with large-scale datasets, has proven its success since the advent of AlexNet [Krizhevsky et al., 2012], achieving remarkable breakthroughs in fields such as computer vision (CV), natural language processing (NLP), robotics, and science. Large-scale datasets like ImageNet [Deng et al., 2009], COCO [Lin et al., 2014], and Kinetics [Kay et al., 2017] have significantly accelerated advancements in these areas. In contrast, the field of Wi-Fi human sensing has not progressed as rapidly, despite the widespread adoption of deep learning methods. A key reason lies in the limited scale and diversity of available Wi-Fi sensing datasets.

Recent initiatives are actively narrowing the data gap; for instance, CSI-Bench [Zhu et al., 2025] achieves a milestone in realism with 461 hours of recordings, XRF55 [Wang et al., 2024] significantly expands the sample count to 42,900, and OctoNet [Yuan et al., 2025] comprises 12 heterogeneous modalities. Despite these advancements in data duration and environmental complexity, Wi-Fi sensing datasets still lack the vast scale of CV benchmarks like ImageNet or Kinetics. The gap remains evident not only in raw sample counts but also in the breadth of action categories and participant demographics, emphasizing the need for continued expansion in data diversity.

Collecting and annotating Wi-Fi sensing data is inherently time-consuming and labor-intensive, creating a data-scarcity bottleneck for deep learning. To address this, synthetic data generation has emerged as a promising solution. By leveraging high-fidelity 3D modeling and computational electromagnetics, researchers can simulate diverse human-environment interactions. For example, by placing dynamic 3D human models into various virtual environments and employing ray-tracing algorithms to emulate signal propagation, realistic Wi-Fi CSI data can be synthesized. This approach provides the massive datasets required to train large-scale foundation models, potentially revolutionizing the scalability of Wi-Fi sensing. However, several open challenges, such as the domain gap between simulated and physical signals, remain to be addressed.

#### Open Challenges in Synthetic Data Generation

1. **Modeling signal propagation:** How to model the propagation of signals through people and environments? Can methods like ray-tracing and Fresnel zone models effectively simulate Wi-Fi signals' interactions with objects and people? How to enable modern approaches, such as diffusion models [Ho et al., 2020], Variational Autoencoders (VAEs) [Kingma & Welling, 2013], Neural Radiance Fields (NeRF) [Mildenhall et al., 2021], or 3D Gaussian Splatting [Kerbl et al., 2023] to learn probabilistic mappings of signal propagation patterns from observed data?

2. **Constructing diverse environments:** Should we rely on manual modeling of environments, even though it is resource-intensive? Or should we leverage open-source tools like Unity, Unreal Engine, or Infinigen Indoors [Raistrick et al., 2024], which provide scalable solutions for generating dynamic, realistic environments tailored to Wi-Fi sensing scenarios?

3. **Synthesizing diverse human body models:** Is it more effective to use game engines like Unity or Unreal Engine to create diverse human models? Alternatively, could tools such as SMPL [Loper et al., 2015] or MANO [Romero et al., 2022] be utilized to extract human body/hand models from large-scale video datasets for synthetic data generation?

4. **Bridging synthetic and real data:** Could Generative Adversarial Networks [Goodfellow et al., 2014] help enhance the realism of synthetic features or adapt synthetic data to better match real-world characteristics? What role could domain adaptation and domain-invariant feature learning play in aligning synthetic and real data to improve model performance?

#### Roadmap for Synthetic Data Generation

* **Short-term Goals (1–2 years):** Focus on enhancing signal realism using advanced generative models (Diffusion Models, GANs). Establish a precise "signal-to-physical-entity" mapping to ensure synthesized CSI samples are indistinguishable from real-world data in both frequency and time domains.

* **Long-term Goals (3–5 years):** Realize large-scale, multi-environment closed-loop simulation systems. Develop simulation engines capable of automatically generating complex 3D indoor scenes and dynamic human-environment interactions. The core challenge is overcoming the "Sim-to-Real" domain gap, ensuring models trained entirely on simulated data can be deployed in physical hardware environments.


### 🐺 Wi-Fi Sensing Foundation Model Pre-Training

Foundation models in vision and language, such as CLIP [Radford et al., 2021], GPT [Brown et al., 2020], and BERT [Devlin et al., 2019], have demonstrated remarkable success in adapting to diverse downstream tasks. Similarly, Wi-Fi sensing encompasses a wide range of applications, including human activity recognition, indoor localization, presence detection, and pose estimation. These varied tasks make the development of a Wi-Fi sensing foundation model both promising and necessary. However, training such a model raises several critical open questions:

#### Open Questions for Foundation Model Design

1. **Model architectures:** Should we utilize traditional architectures like CNNs and RNNs, or opt for Transformers [Vaswani et al., 2017]? Emerging architectures like Mamba [Gu et al., 2023], known for smaller parameters, reduced memory usage, and faster inference, may also be viable. How to tailor architecture design for different hardware constraints?

2. **Leveraging unlabeled real-world data:** How can large-scale unlabeled real-world Wi-Fi data be incorporated effectively? Should data be transmitted to a central server, or processed at the edge? How can privacy and computational constraints be maintained?

3. **Self-supervised learning strategies:** What proxy tasks are most suitable? Contrastive learning, masking-then-reconstruction (as in BERT or MAE [He et al., 2022]), or domain-specific tasks for capturing spatiotemporal Wi-Fi signal characteristics?

4. **Incorporating environmental and human factors:** Should environmental parameters, human body factors, and device configurations be embedded explicitly, or inferred implicitly by the model?

#### Roadmap for Wi-Fi Foundation Models

* **Short-term Goals (1–2 years):** Construct task-agnostic universal feature extractors using self-supervised learning (e.g., Masked Signal Modeling) on medium-scale datasets. Ensure robustness against device heterogeneity.

* **Long-term Goals (3–5 years):** Train large-scale perception foundation models with billions of parameters. Integrate ultra-large-scale unlabeled real-world data with synthetic datasets for zero-shot generalization. Address computational costs and globally distributed device coordination while preserving privacy.


### 🐳 When Wi-Fi Sensing Meets Large Multimodal Models

Another promising direction is leveraging existing large multimodal models (LMMs) by fine-tuning them to process Wi-Fi data. LMMs trained on diverse images, text, and audio demonstrate impressive adaptability. Integrating Wi-Fi raises several challenges:

#### Open Questions

1. **Fine-tuning strategy:** LoRA [Hu et al., 2022], adapters [Rebuffi et al., 2017], or prompt-based fine-tuning [Liu et al., 2021]? How to balance computational efficiency and task performance?

2. **Aligning Wi-Fi with existing modalities:** Should Wi-Fi CSI data be converted to spectrograms/images [Zhang et al., 2023; Jiao et al., 2024] or processed in native time-series format? How to bridge the semantic gap via cross-modal contrastive learning or other alignment techniques?

3. **Incorporating domain knowledge:** Use Wi-Fi propagation principles, IEEE 802.11bf protocols, or Retrieval-Augmented Generation (RAG) [Lewis et al., 2020] for interpretability and efficiency.

4. **Multimodal fusion:** Wi-Fi combined with cameras or IMUs can enhance performance. Techniques like ALBEF [Li et al., 2021], Cross-Attention [Chen et al., 2024], or Mixture of Experts [Yun et al., 2024] may be applied. Challenges include modality-specific noise, temporal synchronization, and computational overhead.

#### Roadmap for LMM Integration

* **Short-term Goals (1–2 years):** Establish efficient semantic alignment between Wi-Fi signals and visual/text modalities. Use cross-modal translation (e.g., WiFi2Radar [Zhang et al., 2020]) to convert Wi-Fi into LMM-compatible tokens.

* **Long-term Goals (3–5 years):** Develop native sensing agents with inherent wireless perception. Bridge the semantic gap between low-level Wi-Fi signals and high-level reasoning in LMMs.


### 🐍 System Deployment

Wi-Fi sensing systems can follow a hierarchical "Cloud-to-Edge" deployment pipeline:

#### Open Challenges

1. **Efficient inference:** Deploying large models on COTS chips (e.g., ESP32) requires handling frequency-domain sparsity. Use structure-aware pruning [Han et al., 2015], quantization [Jacob et al., 2018], and knowledge distillation [Hinton et al., 2015] to retain subcarriers sensitive to human motion.

2. **On-device training and fine-tuning:** Environmental shifts require edge adaptation with on-device training [Lin et al., 2022] to calibrate models to local environments.

3. **Sensing-communication coexistence:** Optimize CSI streaming and resource allocation during congestion via downsampling or temporal-spectral compression. Consider ISAC-aware scheduling.

4. **Adversarial resilience:** Protect against physical adversarial attacks [Liu et al., 2022] and explore Generative AI solutions for physical-layer security (e.g., DFSS [Wang et al., 2025]).

5. **Data collection in consumer scenarios:** Minimize manual labeling via implicit feedback loops and cross-modal supervision (e.g., smartphone IMUs). Challenges include noisy labels, privacy restrictions, and concept drift.

#### Roadmap for Deployment

* **Short-term Goals (1–2 years):** Develop lightweight adaptive deployment, low-power calibration-free algorithms, and standardized sensing interfaces (e.g., IEEE 802.11bf).

* **Long-term Goals (3–5 years):** Realize large-scale, privacy-preserving "Sensing-as-a-Service" integrated into smart city infrastructure.
