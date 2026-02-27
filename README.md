# 🏇 Awesome Wi-Fi Sensing Generalization

[Fei Wang](https://scholar.google.com/citations?user=LKPpmXQAAAAJ), [Tingting Zhang](https://scholar.google.com/citations?user=R7kxvQkAAAAJ), Wei Xi, Han Ding, Ge Wang, Di Zhang, Yuanhao Cui, Fan Liu, Jinsong Han, Jie Xu, Tony Xiao Han, **A Survey on Wi-Fi Sensing Generalizability: Taxonomy, Techniques, Datasets, and Future Research Prospects**, IEEE Communications Surveys & Tutorials， 2026

**Sensing Dataset Platform:** https://sdp8.org/

![fig3](https://github.com/user-attachments/assets/95ff3b85-0965-433c-95dc-449c87cda4e1)
Fig.3 Growth of research in Wi-Fi sensing generalizability: from a handful of studies between year of 2015 and 2018 to a surge of publications since 2019. We employed a linear regression to fit the growth trend. In the figure, the $R^2$ score indicates the correlation between the estimated results and the ground truth, where a value closer to 1 denotes a higher degree of model fitting. (We selected one representative paper per year based on the highest citation count, ensuring each choice employs a technical approach distinct from those featured in previous years.)



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


## :dog: Datasets 

<img width="1781" height="746" alt="fig17" src="https://github.com/user-attachments/assets/aeb2a618-6cc8-4b60-a928-93cc69c80f66" />
Fig. 17 Bubble chart of public Wi-Fi sensing datasets, where the bubble size indicates the number of samples and the vertical axis represents the number of classes. For visual clarity, datasets with extreme values, such as **SignFi** (296 classes) and **CSI-Bench** (over 1,000,000 samples), are excluded from the plot. Besides, datasets like **WiFiTAD**, **MM-Fi**, and **XRFv2**, which collect continuous sequences over time without clear per-sample annotations, are also not included due to the ambiguity in estimating their sample counts.



| ID | Dataset | Main Domain Information | Device Setting | Highlight | Main Results | Download Link |
|---|---|---|---|---|---|---|
| **Action Recognition** |
| 1 | XRF55[1](@ref) | 4 environments, 39 participants, 55 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, 55 actions | 87.26% |https://aiotgroup.github.io/XRF55/ |
| 2 | BullyDetect[2](@ref) | 8 environments, 20 paired participants, 7 actions | 1Tx, 1Rx, 20MHz, 5GHz | Bullying actions | 90.4% |https://github.com/aiotgroup/WiFi-BullyDetect|
| 3 | WiSDA[3](@ref) | 1 environments, 3 participants, 6 actions | 1Tx, 1Rx, 20MHz | Widar3.0-like | 99.5% |https://www.researchgate.net/publication/385918549_WiSDA_Subdomain_Adaptation_Human_Activity_Recognition_Method_Using_Wi-Fi_Signals|
| 4 | WiNDR[4](@ref) | 1 environments, 3 participants, 5 actions, 24 orientation | 1Tx, 1Rx, 20MHz, 5GHz | Full 360° coverage | 78%-92% |https://gitlab.com/yuxiqin/direction-independent|
| 5 | WiMANS[5](@ref) | 3 environments, 6 participants, 9 actions | 1Tx, 1Rx, 20MHz, 2.4/5GHz | Multi-person | 89.1%-96.6% |https://github.com/huangshk/WiMAN|
| 6 | WiGuesture[6](@ref) | 1 environments, 8 participants, 6 actions | 1Tx, 1Rx, 100Hz, 2.4GHz | ESP32S3 | 92.57% |https://github.com/RS2002/CSI-BERT|
| 7 | RoGER[7](@ref) | 2 environments, 4 participants, 6 actions, 4 orientation | 1Tx, 2Rx, 20MHz, 2.437GHz | AR9580 | 94.84%-99.71% |http://bisuzhi.cn/Sensedata.html|
| 8 | ImgFi[8](@ref) | 1 environments, 5 participants, 6 actions | 1Tx, 1Rx, 20MHz | Converted to images | 99.8% |https://ieeexplore.ieee.org/document/10190332|
| 9 | ResMon[9](@ref) | 2 environments, 3 areas, 6 participants, 4 actions | 1Tx, 1Rx, 20/40MHz, 2.4/5GHz | Cross-band test | 83.80%-89.67% |http://bisuzhi.cn/Sensedata.html|
| 10 | Meneghello et al.[10](@ref) | 6 environments, 4 participants, 7 actions | 1Tx, 1Rx, 80MHz, 5.21GHz | 80MHz | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| 11 | Demrozi et al.[11](@ref) | 2 environments, 6 participants, 6 actions | 2Tx, 2Rx, 2.4GHz | Nexmon firmware | 99.3% |https://www.techrxiv.org/doi/full/10.36227/techrxiv.22284421.v1|
| 12 | MM-Fi[12](@ref) | 4 environments, 40 participants, 27actions | 1TX, 1RX, 20MHz, 5GHz | Multimodal | not reported |https://ntu-aiot-lab.github.io/mm-fi|
| 13 | NTU-Fi HAR[13](@ref) | 1 environments, 20 participants, 6 actions | 1Tx, 1Rx, 40MHz, 5GHz | TP-Link N750 | 98.6% |https://github.com/xyanchen/WiFi-CSI-Sensing-Benchmark|
| 14 | FallDar[14](@ref) | 4 environments, 6 locations, 6 participants, fall & normal | 1Tx, 1Rx, 1000Hz, 5GHz | 6 months | 5.7% FAR |http://www.sdp8.net/Dataset?id=dfe4621e-4774-4ef4-b064-e4a082c12335|
| 15 | ReWis[15](@ref) | 3 environments, 2 participants, 4 actions | 1Tx, 3Rx, 20/80MHz, 5GHz | 80MHz | 78.25%-99.82% |https://github.com/niloobah/ReWiS|
| 16 | OPERAnet[16](@ref) | 2 environments, 6 participants, 6 actions | 1Tx, 2Rx, 5GHz | Multimodal | 71%-100% |https://springernature.figshare.com/collections/A_Comprehensive_Multimodal_Activity_Recognition_Dataset_Acquired_from_Radio_Frequency_and_Vision-Based_Sensors/5551209/1|
| 17 | SHARP[17](@ref) | 3 environments, 4 locations, 3 participants, 7 actions | 1Tx, 1Rx, 80MB, 5GHz | 80MHz | 95.99%-99.79% |https://github.com/francescamen/SHARP|
| 18 | CSI-HAR-Dataset[18](@ref) | 1 environments, 3 participants, 7 actions | 1Tx, 1Rx, 20MHz, 5GHz | 802.11ac | 95.5% |https://github.com/parisafm/CSI-HAR-Dataset|
| 19 | CSIDA[19](@ref) | 2 environments, 5 locations, 5 participants, 6 actions | 1Tx, 1Rx, 40MHz, 5GHz | 114 subcarriers | 90.10%±1.03% |https://github.com/Zhang-xie/WiGr|
| 20 | RISE[20](@ref) | 2 environments, 6 participants, 6 actions | 1Tx, 1Rx | multi-rf devices | 93.9%-100% |https://github.com/jiaojiao1234/RISE|
| 21 | HTHI[21](@ref) | 1 environment, 40 paired, 12 actions | 2Tx, 3Rx, 20MHz, 2.4GHz | Human-human actions | not reported |https://data.mendeley.com/datasets/3dhn4xnjxw/1|
| 22 | DeepSeg[22](@ref) | 1 environment, 5 participants, 10 actions | 1Tx, 3Rx | fine-/coarse-grained actions | 94% |https://github.com/ChunjingXiao/DeepSeg|
| 23 | RF-Net[23](@ref) | 6 environments, 11 participants, 6 actions | 2 Tx-Rx pairs, 20MHz | 120 environment | ≈ 80% |https://github.com/di0002ya/RFNet|
| 24 | Baha’A et al.[24](@ref) | 3 environments, 30 participants, 12 actions | 1Tx, 3Rx, 20MHz, 2.4GHz | LOS/NLOS | not reported |http://www.sdp8.net/Dataset?id=dfe4621e-4774-4ef4-b064-e4a082c12335|
| 25 | Widar 3.0[25](@ref) | 3 environments, 5 locations, 5 orientations, 16 participants, 16 actions | 1Tx, 6Rx, 20MHz, 5.825GHz | Rich domains | 92.7%-92.9% |https://tns.thss.tsinghua.edu.cn/widar3.0/|
| 26 | ARIL[26](@ref) | 16 locations, 1 participants, 6 actions | 1Tx, 1Rx, 20MHz, 2.4GHz | USRP data, clean phase | 89.57% |https://github.com/geekfeiw/ARIL|
| 27 | WiAR[27](@ref) | 3 environments, 10 participants, 16 actions | 1Tx, 1Rx, 20MHz, 5GHz | RSSI and CSI | 90.62%-96.25% |https://github.com/linteresa/WiAR|
| 28 | SAR[28](@ref) | 1 environment, 9 participants, 6actions | 2-3Tx, 3Rx, 20MHz, 2.4GHz | 6 days | 60%-100% |https://data.4tu.nl/articles/_/12692816/1|
| 29 | FallDeFi[29](@ref) | 5 environments, 3 participants, 9 actions | 2Tx, 2Rx, 20MHz, 5.2GHz | Fall detection | 80.10%-88.90% |https://github.com/dmsp123/FallDeFi|
| 30 | SignFi[30](@ref) | 2 environments, 5 participants, 276 gestures | 3Tx, 1Rx, 20MHz, 5GHz | 276 ASL Gestures | 94.81%-98.91% |https://github.com/yongsen/SignFi|
| 31 | CrossSense[31](@ref) | 3 environments, 15 locations, 100 participants, 40 actions | 1Tx, 1Rx, 20MHz, 5GHz | 100 participants | 90% |Agreement required https://github.com/nwuzj/CrossSense/|
| 32 | Yousef et al.[32](@ref) | 1 environments, 6 participants, 6 actions | 1Tx, 1Rx, 20MHz, 5GHz | Fall | 81%-97% |https://github.com/ermongroup/Wifi_Activity_Recognition|
| **Gait Recognition** |
| 33 | NTU-Fi HumanID[33](@ref) | 2 environments, 20 participants, walking | 1Tx, 1Rx, 40MHz, 5GHz | TP-Link N750 | 86.29&-98.34% |https://github.com/xyanchen/WiFi-CSI-Sensing-Benchmark|
| 20 | RISE[20](@ref) | 3 environments, 15 participants | 1Tx, 1Rx | multi-rf devices | 97.6% |https://github.com/jiaojiao1234/RISE/|
| 34 | GaitID[34](@ref) | 2 environments, 11 participants, 8 directions | 1Tx, 6Rx | 8 directions | 61%-100% |http://www.sdp8.net/Dataset?id=87a65da2-18cb-4b8f-a1ec-c9696890172b|
| 31 | CrossSense[31](@ref) | 3 environments, 100 participants | 1Tx, 1Rx, 20MHz, 5GHz | 100 participants | 80% |Agreement required https://github.com/nwuzj/CrossSense|
| **Pose Estimation** |
| 35 | XRFv2[35](@ref) | 3 environments, 16 participants, 30 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, continuous actions | not reported |https://github.com/aiotgroup/XRFV2|
| 36 | Person-in-WiFi 3D[36](@ref) | 3 environments, 7 participants, 8actions | 1Tx, 3Rx, 20MHz, 5GHz | Multi-person | 107.2mm MPJPE |https://aiotgroup.github.io/Person-in-WiFi-3D/|
| 1 | XRF55[1](@ref) | 4 environments, 39 participants, 55 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, 55 actions | not reported |https://aiotgroup.github.io/XRF55/|
| 12 | MM-Fi[12](@ref) | 4 environments, 40 participants, 27 actions | 20MHz, 5GHz | Multimodal | 197.1mm MPJPE |https://ntu-aiot-lab.github.io/mm-fi|
| **Indoor Localization** |
| 37 | MetaLoc[37](@ref) | 2 environments, 180 locations | 3Tx, 1Rx, 20MHz, 5GHz | RSSI and CSI | 2.07±1.11m error |https://github.com/StatFusion/MetaLoc|
| 38 | Chen and Chang[38](@ref) | 2 environments, 16 locations | 2Tx, 2Rx | CSI fingerprints | 49.47%-90.44% |https://github.com/BingJiaChen/few-shot-indoor-localization|
| 26 | ARIL[26](@ref) | 1 environments, 16 locations, 1 participants, 6 actions | 1Tx, 1Rx, 20MHz, 2.4GHz | USRP data, clean phase | 95.68% |https://github.com/geekfeiw/ARIL|
| **Crowd Counting** |
| 39 | SDP[39](@ref) | 4 scenarios | multi-APs, 80/160MHz, 5GHz | 0-2 people | not reported |https://sdp8.org/Dataset?id=277beeba-afdc-4bb1-8b47-88fa366fb27d|
| 40 | DASECount[40](@ref) | 2 environments, 2 scenarios (NLOS/LOS), 3 motions | 1Tx, 1Rx, 40MHz, 2.4GHz | 0-8 people | 93.29%-99.17% |http://bisuzhi.cn/Sensedata.html|
| 10 | Meneghello et al.[10](@ref) | 1 environments, 10 participants | 1Tx, 1Rx, 80MHz, 5.21GHz | 1-10 people | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| **Temporal Action Localization, Action Summarization** |
| 35 | XRFv2[35](@ref) | 3 environments, 16 participants, 30 actions | 1Tx, 3Rx, 20MHz, 5GHz | Multimodal, continuous actions | 78.74 mAP |https://github.com/aiotgroup/XRFV2|
| 41 | WiFiTAD[41](@ref) | 1 environment, 3 participants, 7 actions | 1Tx, 1Rx, 5GHz | Continuous actions | 74.5 mAP |https://github.com/AVC2-UESTC/WiFiTAD|
| **Multiple Sub-Datasets** |
| 42 | CSI-Bench[42](@ref) | 26 environments, 35 participants | 16 device configuration | In-the-wild data, 461 hours | 94.88% fall detection, etc. |https://ai-iot-sensing.github.io/projects/project.html|
| 10 | Meneghello et al.[10](@ref) | 7 environments, 13 participants | 1Tx, 1Rx, 80MHz, 5.21GHz | Three tasks, 80MHz | not reported |https://paperswithcode.com/paper/a-csi-dataset-for-wireless-human-sensing-on|
| 43 | CSI-Net[43](@ref) | 1 environments, 5 positions, 30 participants | 1Tx, 1Rx, 20MHz, 5GHz | Four tasks, Biometrics | 96.67% fall detection, etc. |https://github.com/geekfeiw/CSI-Net|


[1](@ref): [wang2024xrf55]
[2](@ref): [lan2024bullydetect]
[3](@ref): [2-1jiao2024wisda]
[4](@ref): [2-10qin2024direction]
[5](@ref): [huang2024wimans]
[6](@ref): [zhao2024finding]
[7](@ref): [2-112bi2024roger]
[8](@ref): [zhang2023imgfi]
[9](@ref): [2-38zheng2023resmon]
[10](@ref): [meneghello2023csi]
[11](@ref): [demrozi2023dataset]
[12](@ref): [yang2024mm]
[13](@ref): [yang2022efficientfi]
[14](@ref): [yang2022rethinking]
[15](@ref): [2-26bahadori2022rewis]
[16](@ref): [bocus2022operanet]
[17](@ref): [2-163meneghello2022sharp]
[18](@ref): [moshiri2021csi]
[19](@ref): [1-6zhang2021wifi]
[20](@ref): [2-94zhai2021rise]
[21](@ref): [alazrai2020dataset]
[22](@ref): [xiao2020deepseg]
[23](@ref): [1-2ding2020rf]
[24](@ref): [baha2020dataset]
[25](@ref): [1-45zheng2019zero]
[26](@ref): [wang2019joint]
[27](@ref): [guo2019wiar]
[28](@ref): [brinke2019dataset,2-161brinke2019scaling]
[29](@ref): [palipana2018falldefi]
[30](@ref): [ma2018signfi]
[31](@ref): [1-50zhang2018crosssense]
[32](@ref): [yousefi2017survey]
[33](@ref): [2-130wang2022caution]
[34](@ref): [2-157zhang2020gaitid]
[35](@ref): [lan2025xrf]
[36](@ref): [yan2024person]
[37](@ref): [2-125gao2023metaloc]
[38](@ref): [2-121chen2022few]
[39](@ref): [tony-sdp-2024]
[40](@ref): [2-36hou2022dasecount]
[41](@ref): [liu2025wifi]
[42](@ref): [zhu2025csi]
[43](@ref): [wang2018csi]



## 🐼 Papers

## Stage 1: 🐘 Experimental Setup 

### Distributed Antennas

\[63\] Y . Qin, S. Sigg, S. Pan, and Z. Li, "Direction-agnostic gesture
recog- nition system using commercial wifi devices,"Computer Communications, vol. 216, pp. 34--44, 2024. [paper](https://www.sciencedirect.com/science/article/pii/S0140366423004747)

\[64\] Y . Qin, S. Pan, and Z. Li, "Cross-domain extendable gesture
recognition system using wifi signals,"Electronics Letters, vol. 59, no.
16, p. e12931, 2023. [paper](https://ietresearch.onlinelibrary.wiley.com/doi/full/10.1049/ell2.12931)

\[65\] F. Wang, W. Gong, and J. Liu, "On spatial diversity in wifi-based
human activity recognition: A deep learning-based approach,"IoT-J,
vol. 6, no. 2, pp. 2035--2047, 2018.


### Distributed Devices

\[66\] N. Bahadori, J. Ashdown, and F. Restuccia, "Rewis: Reliable wi-fi
sensing through few-shot multi-antenna multi-receiver csi learning," in
WoWMoM. IEEE, 2022, pp. 50--59.

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325.

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219.

\[69\] D. Wu, Y . Zeng, R. Gao, S. Li, Y . Li, R. C. Shah, H. Lu, and D.
Zhang, "Witraj: Robust indoor motion tracking with wifi signals,"IEEE
TMC, vol. 22, no. 5, pp. 3062--3078, 2021.

### Scaling Up Dataset

\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024.

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325.

\[71\] Y . Zhang, Y . Yin, Y . Wang, J. Ai, and D. Wu, "Csi-based
location- independent human activity recognition with parallel
convolutional networks,"Computer Communications, vol. 197, pp. 87--95,
2023.

\[72\] J. Yang, H. Huang, Y . Zhou, X. Chen, Y . Xu, S. Yuan, H. Zou, C.
X. Lu, and L. Xie, "Mm-fi: Multi-modal non-intrusive 4d human dataset
for versatile wireless sensing,"NeurIPS, vol. 36, 2024.

\[73\] G. Zhu, Y . Hu, W. Gao, W.-H. Wang, B. Wang, and K. Liu, "Csi-
bench: A large-scale in-the-wild dataset for multi-task wifi sensing,"
arXiv preprint arXiv:2505.21866, 2025.

## Stage 2: :snail: Signal Preprocessing

### Signal Analysis Methods
\[74\] Y . Lu, S. Lv, and X. Wang, "Towards location independent gesture
recognition with commodity wifi devices,"Electronics, vol. 8, no. 10,
p. 1069, 2019.

\[75\] R. Zhou, Z. Gong, K. Tang, B. Zhou, and Y . Cheng, "Device-free
cross location activity recognition via semi-supervised deep
learning,"Neural Computing and Applications, vol. 34, no. 12, pp. 10
189--10 203, 2022.

\[76\] J. Yang, Y . Liu, Y . Wu, P. Yang, and Z. Liu, "Gait-enhance:
Robust gait recognition of complex walking patterns based on wifi csi,"
inSmart World Congress. IEEE, 2023, pp. 1--9.

\[77\] H. Zhuo, X. Wu, Q. Zhong, and H. Zhang, "Position-free breath
detection during sleep via commodity wifi,"IEEE Sensors Journal, 2023.

\[78\] F. Abuhoureyah, S. K. Swee, and W. Y . Chiew, "Multi-user human
activity recognition through adaptive location-independent wifi signal
characteristics,"IEEE Access, 2024.\[79\] W. Meng, X. Chen, W. Cui, and
J. Guo, "Wihgr: A robust wifi-based human gesture recognition system via
sparse recovery and modified attention-based bgru,"IoT-J, vol. 9, no.
12, pp. 10 272--10 282, 2021.

### Advanced Handcrafted Indicators

\[79\] W. Meng, X. Chen, W. Cui, and
J. Guo, "Wihgr: A robust wifi-based human gesture recognition system via
sparse recovery and modified attention-based bgru,"IoT-J, vol. 9, no.
12, pp. 10 272--10 282, 2021.

\[80\] J. Huang, B. Liu, C. Miao, Y . Lu, Q. Zheng, Y . Wu, J. Liu, L.
Su, and C. W. Chen, "Phaseanti: An anti-interference wifi-based activity
recognition system using interference-independent phase component," IEEE
TMC, vol. 22, no. 5, pp. 2938--2954, 2021.

\[81\] R. Gao, W. Li, Y . Xie, E. Yi, L. Wang, D. Wu, and D. Zhang,
"Towards robust gesture recognition by characterizing the sensing
quality of wifi signals,"IMWUT, vol. 6, no. 1, pp. 1--26, 2022.

\[82\] J. Zhang, Y . Li, H. Xiong, D. Dou, C. Miao, and D. Zhang,
"Handgest: Hierarchical sensing for robust-in-the-air handwriting
recognition with commodity wifi devices,"IoT-J, vol. 9, no. 19, pp. 19
529--19 544, 2022.

\[83\] X. Yu, T. Jiang, X. Ding, Z. Yao, X. Zhou, and Y . Zhong,
"Towards position-independent gesture recognition based on wifi by
subcarrier selection and gesture code," inWCNC. IEEE, 2023, pp. 1--6.

\[84\] Y . Zhang, Q. Liu, Y . Wang, and G. Yu, "Csi-based
location-independent human activity recognition using feature
fusion,"IEEE TIM, vol. 71, pp. 1--12, 2022.

\[85\] C. Peng, L. Gui, B. Sheng, Z. Guo, and F. Xiao, "Rosefi: A robust
sedentary behavior monitoring system with commodity wifi devices," IEEE
TMC, 2023.

\[86\] X. Wang, A. Yu, K. Niu, W. Shi, J. Wang, Z. Yao, R. C. Shah, H.
Lu, and D. Zhang, "Understanding the diffraction model in static
multipath- rich environments for wifi sensing system design,"IEEE TMC,
2024.

\[87\] X. Ding, X. Yu, Y . Zhong, W. Xie, B. Cai, M. You, and T. Jiang,
"Robust gesture recognition method toward intelligent environment using
wi-fi signals,"Measurement, vol. 231, p. 114525, 2024.

\[88\] M. Peng, X. Fu, H. Zhao, Y . Wang, and C. Kai, "Likey: Location-
independent keystroke recognition on numeric keypads using wifi
signal,"Computer Networks, vol. 245, p. 110354, 2024.

\[89\] Q. Bu, G. Yang, J. Feng, and X. Ming, "Wi-fi based gesture
recognition using deep transfer learning," inSmartWorld, Ubiquitous
Intelligence & Computing, Advanced & Trusted Computing, Scalable
Computing & Communications, Cloud & Big Data Computing, Internet of
People and Smart City Innovation. IEEE, 2018, pp. 590--595.

\[90\] C. Zhang, W. Jiao, and W. Du, "Enhancing human activity
recognition performance in small-sample wi-fi sensing using data
augmentation methods," inICCT. IEEE, 2023, pp. 473--478.

### Motion Indicators

\[91\] F. Meneghello, D. Garlisi, N. Dal Fabbro, I. Tinnirello, and M.
Rossi, "Sharp: Environment and person independent activity recognition
with commodity ieee 802.11 access points,"IEEE TMC, vol. 22, no. 10,
pp. 6160--6175, 2022.

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240.

\[93\] Y . Yin, Z. Zhang, X. Yang, F. Yan, and Q. Niu, "Towards fully
domain- independent gesture recognition using cots wifi
device,"Electronics Letters, vol. 57, no. 5, pp. 232--234, 2021.

\[94\] C. Feng, N. Wang, Y . Jiang, X. Zheng, K. Li, Z. Wang, and X.
Chen, "Wi-learner: Towards one-shot learning for cross-domain wi-fi
based gesture recognition,"IMWUT, vol. 6, no. 3, pp. 1--27, 2022.

\[95\] K. Niu, F. Zhang, X. Wang, Q. Lv, H. Luo, and D. Zhang, "Under-
standing wifi signal frequency features for position-independent gesture
sensing,"IEEE TMC, vol. 21, no. 11, pp. 4156--4171, 2021.

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024.

\[97\] S. Li, Z. Liu, Q. Lv, Y . Zou, Y . Zhang, and D. Zhang, "Wilife:
Long-term daily status monitoring and habit mining of the elderly
leveraging ubiquitous wi-fi signals,"ACM Transactions on Computing for
Healthcare.

\[98\] B. van Berlo, C. Oerlemans, F. L. Marogna, T. Ozcelebi, and N.
Merat- nia, "Mini-batch alignment: A deep-learning model for domain
factor- independent feature extraction for wi-fi--csi data,"Sensors,
vol. 23, no. 23, p. 9534, 2023.

\[99\] B. van Berlo, T. Ozcelebi, and N. Meratnia, "Insights on mini-
batch alignment for wifi-csi data domain factor independent feature
extraction," inInternational Conference on Pervasive Computing and
Communications Workshops and other Affiliated Event. IEEE, 2022,
pp. 527--532.

\[69\] D. Wu, Y . Zeng, R. Gao, S. Li, Y . Li, R. C. Shah, H. Lu, and D.
Zhang, "Witraj: Robust indoor motion tracking with wifi signals,"IEEE
TMC, vol. 22, no. 5, pp. 3062--3078, 2021.

\[67\] Y . Zheng, Y . Zhang, K. Qian, G. Zhang, Y . Liu, C. Wu, and Z.
Yang, "Zero-effort cross-domain gesture recognition with wi-fi,"
inMobiSys, 2019, pp. 313--325.

\[100\] B.-B. Zhang, D. Zhang, Y . Hu, and Y . Chen, "Unsupervised
domain adaptation for wifi gesture recognition," inWCNC. IEEE, 2023,
pp. 1--6.

\[101\] M. Yang, H. Zhu, R. Zhu, F. Wu, L. Yin, and Y . Yang,
"Witransformer: A novel robust gesture recognition sensing model with
wifi,"Sensors, vol. 23, no. 5, p. 2612, 2023.

\[102\] W. Shi, M. Duan, H. He, L. Lin, C. Yang, C. Li, and J. Zhao,
"Location adaptive motion recognition based on wi-fi feature
enhancement," Applied Sciences, vol. 13, no. 3, p. 1320, 2023.

\[103\] I. Bulugu, "Gesture recognition system based on cross-domain csi
extracted from wi-fi devices combined with the 3d cnn,"Signal, Image and
Video Processing, vol. 17, no. 6, pp. 3201--3209, 2023.

\[30\] Y . Zhang, Y . Zheng, G. Zhang, K. Qian, C. Qian, and Z. Yang,
"Gaitid: Robust wi-fi based gait recognition," inWASA. Springer, 2020,
pp. 730--742.

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219.

\[104\] G. Chi, G. Zhang, X. Ding, Q. Ma, Z. Yang, Z. Du, H. Xiao, and
Z. Liu, "Xfall: Domain adaptive wi-fi-based fall detection with cross-
modal supervision,"IEEE JASAC, 2024.

\[105\] R. Gao, M. Zhang, J. Zhang, Y . Li, E. Yi, D. Wu, L. Wang, and
D. Zhang, "Towards position-independent sensing for gesture recogni-
tion with wi-fi,"IMWUT, vol. 5, no. 2, pp. 1--28, 2021.

\[106\] C. Shi, J. Liu, N. Borodinov, B. Leao, and Y . Chen, "Towards
environment-independent behavior-based user authentication using wifi,"
inMASS. IEEE, 2020, pp. 666--674.

\[107\] Y . Wang, Y . Tian, and R. Peng, "Position and orientation
independent wireless gesture recognition," inWCSP. IEEE, 2022,
pp. 466--471.

\[108\] D. Wu, D. Zhang, C. Xu, Y . Wang, and H. Wang, "Widir: Walking
direction estimation using wireless signals," inUBICOMP, 2016,
pp. 351--362.

\[109\] H. Wang, D. Zhang, J. Ma, Y . Wang, Y . Wang, D. Wu, T. Gu, and
B. Xie, "Human respiration detection with commodity wifi devices: Do
user location and body orientation matter?" inUBICOMP, 2016, pp. 25--36.

\[63\] Y . Qin, S. Sigg, S. Pan, and Z. Li, "Direction-agnostic gesture
recog- nition system using commercial wifi devices,"Computer Communica-
tions, vol. 216, pp. 34--44, 2024.

\[110\] L. Zhang, C. Wang, M. Ma, and D. Zhang, "Widigr: Direction-
independent gait recognition system using commercial wi-fi devices,"
IoT-J, vol. 7, no. 2, pp. 1178--1191, 2019.

\[111\] L. Zhang, C. Wang, and D. Zhang, "Wi-pigr: Path independent gait
recognition with commodity wi-fi,"IEEE TMC, vol. 21, no. 9,
pp. 3414--3427, 2021.

\[112\] F. Zhang, C. Wu, B. Wang, H.-Q. Lai, Y . Han, and K. R. Liu,
"Widetect: Robust motion detection with a statistical electromagnetic
model," IMWUT, vol. 3, no. 3, pp. 1--24, 2019.

\[113\] G. Zhu, B. Wang, W. Gao, Y . Hu, C. Wu, and K. R. Liu,
"Wifi-based robust human and non-human motion recognition with deep
learning," inPerCom Workshops. IEEE, 2024, pp. 769--774.

### Angle Indicators

\[114\] Y . Li, T. Jiang, X. Ding, and Y . Wang, "Location-free csi
based activity recognition with angle difference of arrival," inWCNC.
IEEE, 2020, pp. 1--6.

\[115\] Z. Han, Z. Lu, Z. Hu, Y . Chen, and X. Wen, "On
position-independency passive gesture tracking with commodity
wi-fi,"IEEE Sensors Journal, vol. 23, no. 14, pp. 16 264--16 275, 2023.

\[116\] Y . Ren and J. Yang, "Robust person identification: A wifi
vision-based approach,"arXiv preprint arXiv:2210.00127, 2022.


## Stage 3: 🦊 Feature Learning

### Domain Alignment

#### Domain Alignment with Domain Discriminator
\[117\] Z. Wang, S. Chen, W. Yang, and Y . Xu, "Environment-independent
wi-fi human activity recognition with adversarial network," inICASSP.
IEEE, 2021, pp. 3330--3334.

\[118\] L. Sheng, Y . Chen, S. Ning, S. Wang, B. Lian, and Z. Wei, "Da-
har: Dual adversarial network for environment-independent wifi human
activity recognition,"Pervasive and Mobile Computing, vol. 96,
p. 101850, 2023.

\[119\] L. Zhang, W. Cui, B. Li, Z. Chen, M. Wu, and T. S. Gee,
"Privacy- preserving cross-environment human activity recognition,"IEEE
Trans- actions on Cybernetics, vol. 53, no. 3, pp. 1765--1775, 2021.

\[120\] Z. Zhou, F. Wang, and W. Gong, "i-sample: Augment domain adver-
sarial adaptation models for wifi-based har,"ACM ToSN, vol. 20, no. 2,
pp. 1--20, 2024.

\[121\] H. Zou, J. Yang, Y . Zhou, and C. J. Spanos, "Joint adversarial
domain adaptation for resilient wifi-enabled device-free gesture
recognition," inICMLA. IEEE, 2018, pp. 202--207.

\[122\] X. Li, L. Chang, F. Song, J. Wang, X. Chen, Z. Tang, and Z.
Wang, "Crossgr: Accurate and low-cost cross-target gesture recognition
using wi-fi,"IMWUT, vol. 5, no. 1, pp. 1--23, 2021.

\[123\] H. Zhang, Z. Zhou, and W. Gong, "Wi-adaptor: Fine-grained domain
adaptation in wifi-based activity recognition," inGLOBECOM. IEEE, 2021,
pp. 1--6.


#### Domain Alignment with Domain Classifier
\[124\] W. Jiang, C. Miao, F. Ma, S. Yao, Y . Wang, Y . Yuan, H. Xue, C.
Song, X. Ma, D. Koutsonikolas, W. Xu, and L. Su, "Towards environment
independent device free human activity recognition," inMobiCom, 2018,
pp. 289--304.

\[125\] A. Khattak and A. Khan, "Cross-location activity recognition
using adversarial learning," inSOICT, 2022, pp. 59--65.

\[126\] F. Wang, J. Liu, and W. Gong, "Wicar: Wifi-based in-car activity
recog- nition with multi-adversarial domain adaptation," inIWQoS, 2019,
pp. 1--10.\[127\] X. Zhang, Y . Feng, J. Huang, H. Yan, P. Zhao, J. Liu,
T. Liu, M. Li, Z. Liu, and B. Liu, "Objective gesture recognition based
on wifi," Authorea Preprints, 2024.

\[128\] A. Zinys, B. van Berlo, and N. Meratnia, "A domain-independent
generative adversarial network for activity recognition using wifi csi
data,"Sensors, vol. 21, no. 23, p. 7852, 2021.

\[129\] J. Strohmayer, R. Sterzinger, M. W ¨odlinger, and M. Kampel,
"Datta: Domain-adversarial test-time adaptation for cross-domain
wifi-based human activity recognition,"arXiv preprint arXiv:2411.13284,
2024.

\[130\] S. Liu, Z. Chen, M. Wu, C. Liu, and L. Chen, "Wisr: Wireless
domain generalization based on style randomization,"IEEE TMC, 2023.

\[93\] Y . Yin, Z. Zhang, X. Yang, F. Yan, and Q. Niu, "Towards fully
domain- independent gesture recognition using cots wifi
device,"Electronics Letters, vol. 57, no. 5, pp. 232--234, 2021.

\[131\] W. Yang, X. Jiawei, W. Ao, X. Huijuan, Z. Chuanxin, and J. Yimu,
"Domain-generalization human activity recognition model based on csi
instance normalization."Journal on Communication/Tongxin Xuebao,
vol. 45, no. 6, 2024.

\[64\] Y . Qin, S. Pan, and Z. Li, "Cross-domain extendable gesture
recognition system using wifi signals,"Electronics Letters, vol. 59, no.
16, p. e12931, 2023.

\[132\] B. v. Berlo, R. Verhoeven, and N. Meratnia, "Use of domain
labels dur- ing pre-training for domain-independent wifi-csi gesture
recognition," Sensors, vol. 23, no. 22, p. 9233, 2023.

\[133\] S. Zhou, L. Guo, Z. Lu, X. Wen, W. Zheng, and Y . Wang,
"Subject- independent human pose image construction with commodity
wi-fi," inIEEE ICC, 2021, pp. 1--6.

\[134\] D. Yan, P. Yang, F. Shang, F. Han, Y . Yan, and X.-Y . Li,
"freegait: Liberalizing wireless-based gait recognition to mitigate
non-gait human behaviors," inMobiHoc, 2024, pp. 241--250.

\[135\] H. Li, X. Chen, J. Wang, D. Wu, and X. Liu, "Dafi: Wifi-based
device- free indoor localization via domain adaptation,"IMWUT, vol. 5,
no. 4, pp. 1--21, 2021.

\[106\] C. Shi, J. Liu, N. Borodinov, B. Leao, and Y . Chen, "Towards
environment-independent behavior-based user authentication using wifi,"
inMASS. IEEE, 2020, pp. 666--674.

\[136\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fidora:
Robust wifi-based indoor localization via unsupervised domain
adaptation," IoT-J, vol. 9, no. 12, pp. 9872--9888, 2022.


#### Domain Alignment with Similarity Computing
\[137\] A. Gretton, K. Borgwardt, M. Rasch, B. Sch ¨olkopf, and A.
Smola, "A kernel method for the two-sample-problem,"NeurIPS, vol. 19,
2006.

\[138\] Y . Zhou, J. Yang, H. Huang, and L. Xie, "Adapose: Towards
cross-site device-free human pose estimation with commodity wifi,"IoT-J,
2024.

\[139\] X. Rao, L. Qin, Y . Yi, J. Liu, G. Lei, and Y . Cao, "A novel
adaptive device-free passive indoor fingerprinting localization under
dynamic environment,"IEEE TNSM, 2024.

\[140\] H. Kang, Q. Zhang, and Q. Huang, "Context-aware wireless-based
cross-domain gesture recognition,"IoT-J, vol. 8, no. 17, pp. 13 503-- 13
515, 2021.

\[141\] Y . Liang, W. Wu, H. Li, F. Han, Z. Liu, P. Xu, X. Lian, and X.
Chen, "Wiai-id: Wi-fi-based domain adaptation for appearance-independent
passive person identification,"IoT-J, vol. 11, no. 1, pp. 1012--1027,
2023.

\[142\] S. Zhang, T. Jiang, X. Ding, X. Zhou, and Y . Zhong,
"Device-free cross-environment human action recognition using wi-fi
signals," in International Conference on Artificial Intelligence in
China. Springer, 2023, pp. 141--151.

\[143\] S. Mehryar, "A domain adaptation framework for human activity
monitoring using passive wi-fi sensing," inICCCMLA. IEEE, 2023,
pp. 263--268.

\[144\] R. Zhou, H. Hou, Z. Gong, Z. Chen, K. Tang, and B. Zhou,
"Adaptive device-free localization in dynamic environments through
adaptive neural networks,"IEEE Sensors Journal, vol. 21, no. 1,
pp. 548--559, 2020.

\[145\] Z. Xiao, S. Zhou, X. Wen, S. Ling, and X. Yang,
"Pattern-independent human gait identification with commodity wifi,"
inWCNC. IEEE, 2024, pp. 1--6.

\[146\] G. Kang, L. Jiang, Y . Yang, and A. G. Hauptmann, "Contrastive
adaptation network for unsupervised domain adaptation," inCVPR, 2019,
pp. 4893--4902.

\[147\] W. Cui, K. Wu, M. Wu, X. Li, and Z. Chen, "Wicau: Comprehen-
sive partial adaptation with uncertainty-aware for wifi-based cross-
environment activity recognition,"IEEE TIM, vol. 73, pp. 1--10, 2024.

\[148\] W. Jiao, C. Zhang, W. Du, and S. Ma, "Wisda: Subdomain
adaptation human activity recognition method using wi-fi signals,"IEEE
TMC, 2024.

\[149\] K. Gong, Y . Gao, and W. Dong, "Privacy-preserving and cross-
domain human sensing by federated domain adaptation with semantic
knowledge correction,"IMWUT, vol. 8, no. 1, pp. 1--26, 2024.

\[150\] B. Sheng, R. Han, H. Cai, F. Xiao, L. Gui, and Z. Guo, "Cdfi:
Cross- domain action recognition using wifi signals,"IEEE TMC, 2024.

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024.

\[151\] X. Zhan and Z. Wu, "Indoor positioning based on channel state
information and deep learning domain adaptation," inICCAID, vol. 13105.
SPIE, 2024, pp. 918--930.

\[152\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Airfi: empowering
wifi-based passive human gesture recognition to unseen environment via
domain generalization,"IEEE TMC, vol. 23, no. 2, pp. 1156--1168, 2022.

\[153\] X. Ding, T. Jiang, Y . Li, W. Xue, and Y . Zhong, "Device-free
location- independent human activity recognition using transfer learning
based on cnn," inICC Workshops. IEEE, 2020, pp. 1--6.

#### Domain Alignment with Generative Adversarial Networks
\[154\] J. Zhang, Z. Chen, C. Luo, B. Wei, S. S. Kanhere, and J. Li,
"Metaganfi: Cross-domain unseen individual identification using wifi
signals,"IMWUT, vol. 6, no. 3, pp. 1--21, 2022.

\[155\] H. Zhang, X. Chen, and S. Chen, "Cross-domain wi-fi sign
language recognition with gans," inICCBN, 2022, pp. 60--65.

\[156\] Y . Mao, Z. Guo, B. Sheng, L. Gui, and F. Xiao, "Wi-cro:
Wifi-based cross domain activity recognition via modified gan,"IEEE TVT,
2024.

\[157\] C. Xiao, Y . Lei, C. Liu, and J. Wu, "Mean teacher-based
cross-domain activity recognition using wifi signals,"IoT-J, vol. 10,
no. 14, pp. 12 787--12 797, 2023.

#### Domain Alignment with Multi-task Learning
\[158\] J. Zhang, Z. Tang, M. Li, D. Fang, P. Nurmi, and Z. Wang,
"Crosssense: Towards cross-site and large-scale wifi sensing,"
inMobiCom, 2018, pp. 305--320.

\[159\] Y . Sugimoto, H. Rizk, A. Uchiyama, and H. Yamaguchi, "Towards
environment-independent activity recognition using wi-fi csi with an
encoder-decoder network," inBodySys, 2023, pp. 13--18.

\[160\] Y . Zhang, A. Cheng, B. Chen, Y . Wang, and L. Jia, "A location-
independent human activity recognition method based on csi: System,
architecture, implementation,"IEEE TMC, 2023.

#### Domain Alignment with Cross-modal Embedding
\[161\] M. T. Islam and S. Nirjon, "Wi-fringe: Leveraging text semantics
in wifi csi-based device-free named gesture recognition," inDCOSS. IEEE,
2020, pp. 35--42.

\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024.

\[162\] H. Zhang, Y . Ren, H. Yuan, J. Zhang, and Y . Shen, "Wi-chat:
Large lan- guage model powered wi-fi sensing,"arXiv preprint
arXiv:2502.12421, 2025.

\[163\] I. Nirmal, A. Khamis, M. Hassan, W. Hu, R. Li, and A.
Kalyanaraman, "Wifi2radar: Orientation-independent single-receiver wifi
sensing via wifi to radar translation,"IoT-J, vol. 11, no. 9, pp. 15
750--15 766, 2024.


### Component Disentangle
\[164\] I. Elujide, C. Feng, A. Shiran, J. Li, and Y . Liu, "Location
indepen- dent gesture recognition using channel state information,"
inAnnual Consumer Communications & Networking Conference. IEEE, 2022,
pp. 841--846.

\[165\] Y .-J. Chen, W. Chen, S. Q. Zhang, H.-Y . Huang, and H. Kung, "A
task- oriented deep learning approach for human localization,"IEEE TCDS,
2024.

\[45\] F. Wang, S. Zhou, S. Panev, J. Han, and D. Huang,
"Person-in-wifi: Fine-grained person perception using wifi," inICCV,
2019, pp. 5452-- 5461.

\[166\] Z. Hao, J. Niu, X.-c. Dang, and Z. Qiao, "Wi-piga: A personnel-
independentmethod for actions recognition based on wi-fi," inBigCom.
IEEE, 2021, pp. 52--59.

\[167\] B. Wu, T. Jiang, J. Yu, X. Ding, S. Wu, and Y . Zhong,
"Device-free human activity recognition with identity-based transfer
mechanism," in WCNC. IEEE, 2021, pp. 1--6.


### Metric Learning for Zero/Few-shot Learning

#### Metric Learning with Triplet Loss
\[167\] B. Wu, T. Jiang, J. Yu, X. Ding, S. Wu, and Y . Zhong,
"Device-free human activity recognition with identity-based transfer
mechanism," in WCNC. IEEE, 2021, pp. 1--6.

\[168\] Q. Zhou, Q. Yang, and J. Xing, "Enabling efficient wifi-based
occupant behavior recognition using insufficient samples,"Building and
Environ- ment, vol. 212, p. 108806, 2022.

\[169\] Z. Wei, W. Chen, W. Tao, S. Ning, B. Lian, X. Sun, and J. Zhao,
"Catfsid: A few-shot human identification system based on cross- domain
adversarial training,"Computer Communications, vol. 224, pp. 275--284,
2024.

\[170\] Q. Bu, X. Ming, J. Hu, T. Zhang, J. Feng, and J. Zhang,
"Transfersense: towards environment independent and one-shot wifi
sensing,"Personal and Ubiquitous Computing, pp. 1--19, 2022.

\[171\] Y . Liu, A. Yu, L. Wang, B. Guo, Y . Li, E. Yi, and D. Zhang,
"Unifi: A unified framework for generalizable gesture recognition with
wi-fi signals using consistency-guided multi-view networks,"IMWUT,
vol. 7, no. 4, pp. 1--29, 2024.

\[172\] X. Zhang, J. Huang, H. Yan, P. Zhao, G. Zhuang, Z. Liu, and B.
Liu, "Wiopen: A robust wi-fi-based open-set gesture recognition
framework,"arXiv preprint arXiv:2402.00822, 2024.

\[173\] Z. Wu, A. A. Efros, and S. X. Yu, "Improving generalization via
scalable neighborhood component analysis," inECCV, 2018, pp. 685-- 701.

\[174\] C. Xiao, S. Chen, F. Zhou, and J. Wu, "Self-supervised few-shot
time-series segmentation for activity recognition,"IEEE TMC, vol. 22,
no. 11, pp. 6770--6783, 2022.

#### Learning with Contrastive Learning
\[175\] K. Xu, J. Wang, L. Zhang, H. Zhu, and D. Zheng, "Dual-stream
contrastive learning for channel state information based human activity
recognition,"JBHI, vol. 27, no. 1, pp. 329--338, 2022.

\[176\] Y . Wang, G. Yu, Y . Zhang, D. Liu, and Y . Zhang, "Csi-based
location- independent human activity recognition by contrast between
dual stream fusion features,"IEEE Sensors Journal, 2024.

\[177\] C. Xiao,
Y . Han, W. Yang, Y . Hou, F. Shi, and K. Chetty, "Diffusion model-based
contrastive learning for human activity recognition,"IoT- J, 2024.

#### Metric Learning with Siamese Neural Networks
\[116\] Y . Ren and J. Yang, "Robust person identification: A wifi
vision-based approach,"arXiv preprint arXiv:2210.00127, 2022.

\[178\] Y . Liang, H. Li, W. Wu, and P. Xu, "Map-sgan: Multi-anchor
point siamese gan for wi-fi csi-based cross-domain gait
recognition,"ESWA, vol. 251, p. 124083, 2024.

\[179\] Z. Zhao, T. Chen, Z. Cai, X. Li, H. Li, Q. Chen, and G. Zhu,
"Crossfi: A cross domain wi-fi sensing framework based on siamese
network," arXiv preprint arXiv:2408.10919, 2024.


#### Metric Learning with Relation Network
\[180\] J. Wang, Q. Gao, X. Ma, Y . Zhao, and Y . Fang, "Learning to
sense: Deep learning for wireless sensing with less training
efforts,"IEEE Wireless Communications, vol. 27, no. 3, pp. 156--162,
2020.

\[181\] P. Hu, C. Tang, K. Yin, and X. Zhang, "Wigr: a practical wi-fi-
based gesture recognition system with a lightweight few-shot network,"
Applied Sciences, vol. 11, no. 8, p. 3329, 2021.

\[182\] L. Zhang, S. Wu, T. Zhang, and Q. Zhang, "Learning to locate:
Adaptive fingerprint-based localization with few-shot relation learning
in dynamic indoor environments,"IEEE TWC, vol. 22, no. 8, pp. 5253--
5264, 2023.

\[183\] R. Zhang, C. Jiang, S. Wu, Q. Zhou, X. Jing, and J. Mu, "Wi-fi
sensing for joint gesture recognition and human identification from few
samples in human-computer interaction,"IEEE JASAC, vol. 40, no. 7,
pp. 2193-- 2205, 2022.

#### Metric Learning with Matching Network
\[184\] Z. Shi, Q. Cheng, J. A. Zhang, and R. Y . Da Xu,
"Environment-robust wifi-based human activity recognition using enhanced
csi and deep learning,"IoT-J, vol. 9, no. 24, pp. 24 643--24 654, 2022.

\[185\] Z. Shi, J. A. Zhang, R. Xu, Q. Cheng, and A. Pearce, "Towards
environment-independent human activity recognition using deep learn- ing
and enhanced csi," inIEEE GLOBECOM. IEEE, 2020, pp. 1--6.

\[186\] Z. Shi, J. A. Zhang, R. Y . Xu, and Q. Cheng,
"Environment-robust device-free human activity recognition with
channel-state-information enhancement and one-shot learning,"IEEE TMC,
vol. 21, no. 2, pp. 540--554, 2020.

\[188\] X. Ding, T. Jiang, Y . Zhong, Y . Huang, and Z. Li, "Wi-fi-based
location-independent human activity recognition via meta learning,"
Sensors, vol. 21, no. 8, p. 2654, 2021.

#### Metric Learning with Prototypical Network
\[66\] N. Bahadori, J. Ashdown, and F. Restuccia, "Rewis: Reliable wi-fi
sensing through few-shot multi-antenna multi-receiver csi learning," in
WoWMoM. IEEE, 2022, pp. 50--59.

\[189\] X. Ding, T. Jiang, Y . Zhong, J. Yang, Y . Huang, and Z. Li,
"Device-free location-independent human activity recognition via
few-shot learning," inIEEE/CIC ICC in China, 2021, pp. 106--111.

\[190\] Y . Gu, H. Yan, M. Dong, M. Wang, X. Zhang, Z. Liu, and F. Ren,
"Wione: one-shot learning for environment-robust device-free user
authentication via commodity wi-fi in man--machine system,"IEEE
Transactions on Computational Social Systems, vol. 8, no. 3, pp. 630--
642, 2021.

\[191\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Caution: A robust
wifi- based human authentication system via few-shot open-set
recognition," IoT-J, vol. 9, no. 18, pp. 17 323--17 333, 2022.

\[192\] B. Yang, H. Wang, L. Hu, H. Zhu, C.-T. Lam, and K. Fang,
"Few-shot cross-domain based wifi sensing system for online learning in
iot," IEEE Sensors Journal, 2023.

\[187\] T. Zhao, N. Wang, G. Cao, S. Mao, and X. Wang, "Functional data
analysis assisted cross-domain wi-fi sensing using few-shot learning,"
inIEEE ICC. IEEE, 2024, pp. 4780--4785.

\[193\] X. Zhang, C. Tang, K. Yin, and Q. Ni, "Wifi-based cross-domain
gesture recognition via modified prototypical networks,"IoT-J, vol. 9,
no. 11, pp. 8584--8596, 2021.

### Meta Learning for Few-shot Learning
\[194\] C. Finn, P. Abbeel, and S. Levine, "Model-agnostic meta-learning
for fast adaptation of deep networks," inICML. PMLR, 2017, pp. 1126--
1135.

\[195\] S. Huang, Y . Chen, D. Wu, G. Yu, and Y . Zhang, "Few-shot
learning for human activity recognition based on csi," inCACML. IEEE,
2022, pp. 403--409.

\[196\] Z. Zhou, F. Wang, J. Yu, J. Ren, Z. Wang, and W. Gong, "Target-
oriented semi-supervised domain adaptation for wifi-based har," in IEEE
INFOCOM. IEEE, 2022, pp. 420--429.

\[197\] J. Gao, D. Wu, F. Yin, Q. Kong, L. Xu, and S. Cui, "Metaloc:
Learning to learn wireless localization,"IEEE JASAC, 2023.

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240.

\[94\] C. Feng, N. Wang, Y . Jiang, X. Zheng, K. Li, Z. Wang, and X.
Chen, "Wi-learner: Towards one-shot learning for cross-domain wi-fi
based gesture recognition,"IMWUT, vol. 6, no. 3, pp. 1--27, 2022.

\[198\] B. Sheng, R. Han, F. Xiao, Z. Guo, and L. Gui, "Metaformer:
Domain- adaptive wifi sensing with only one labelled target
sample,"IMWUT, vol. 8, no. 1, pp. 1--27, 2024.

\[199\] S. Ding, Z. Chen, T. Zheng, and J. Luo, "Rf-net: A unified meta-
learning framework for rf-enabled one-shot human activity recogni-
tion," inSenSys, 2020, pp. 517--530.

\[154\] J. Zhang, Z. Chen, C. Luo, B. Wei, S. S. Kanhere, and J. Li,
"Metaganfi: Cross-domain unseen individual identification using wifi
signals,"IMWUT, vol. 6, no. 3, pp. 1--21, 2022.

\[200\] Z. Gao, J. Xue, J. Zhang, and W. Xiao, "Ml-wigr: A
meta-learning- based approach for cross-domain device-free gesture
recognition,"Soft Computing, vol. 26, no. 13, pp. 6145--6155, 2022.

### Data Augmentationand Data Synthesize
\[122\] X. Li, L. Chang, F. Song, J. Wang, X. Chen, Z. Tang, and Z.
Wang, "Crossgr: Accurate and low-cost cross-target gesture recognition
using wi-fi,"IMWUT, vol. 5, no. 1, pp. 1--23, 2021.

\[180\] J. Wang, Q. Gao, X. Ma, Y . Zhao, and Y . Fang, "Learning to
sense: Deep learning for wireless sensing with less training
efforts,"IEEE Wireless Communications, vol. 27, no. 3, pp. 156--162,
2020.

\[201\] Y . Zhang, X. Wang, Y . Wang, and H. Chen, "Human activity
recogni- tion across scenes and categories based on csi,"IEEE TMC, 2020.

\[202\] J. Zhang, Y . Dai, J. Chen, C. Luo, B. Wei, V . C. Leung, and J.
Li, "Sida: Self-supervised imbalanced domain adaptation for sound
enhancement and cross-domain wifi sensing,"IMWUT, vol. 7, no. 3,
pp. 1--24, 2023.

\[203\] T. Huang, S. Wang, and S. Li, "Low-cost and user independent
action recognition using wifi signals,"Available at SSRN 4160593.

\[182\] L. Zhang, S. Wu, T. Zhang, and Q. Zhang, "Learning to locate:
Adaptive fingerprint-based localization with few-shot relation learning
in dynamic indoor environments,"IEEE TWC, vol. 22, no. 8, pp. 5253--
5264, 2023.

\[204\] Y . Wang, L. Yao, Y . Wang, and Y . Zhang, "Robust csi-based
human activity recognition with augment few shot learning,"IEEE Sensors
Journal, vol. 21, no. 21, pp. 24 297--24 308, 2021.

\[205\] L. Zhang, Y . Jiang, Y . Ma, S. Mao, W. Huang, Z. Yu, X. Zheng,
L. Shu, X. Fan, and G. Xu, "Toward robust and effective behavior based
user authentication with off-the-shelf wi-fi,"IEEE TIFS, 2024.

\[136\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fidora:
Robust wifi-based indoor localization via unsupervised domain
adaptation," IoT-J, vol. 9, no. 12, pp. 9872--9888, 2022.

\[206\] C. Xiao, D. Han, Y . Ma, and Z. Qin, "Csigan: Robust channel
state information-based activity recognition with gans,"IoT-J, vol. 6,
no. 6, pp. 10 191--10 204, 2019.

\[207\] X. Chen, H. Li, C. Zhou, X. Liu, D. Wu, and G. Dudek, "Fido:
Ubiquitous fine-grained wifi-based localization for unlabelled users via
domain adaptation," inProceedings of The Web Conference, 2020,
pp. 23--33.

\[134\] D. Yan, P. Yang, F. Shang, F. Han, Y . Yan, and X.-Y . Li,
"freegait: Liberalizing wireless-based gait recognition to mitigate
non-gait human behaviors," inMobiHoc, 2024, pp. 241--250.

\[177\] C. Xiao,
Y . Han, W. Yang, Y . Hou, F. Shi, and K. Chetty, "Diffusion model-based
contrastive learning for human activity recognition,"IoT- J, 2024.

\[208\] D. Yan, F. Shang, P. Yang, F. Han, Y . Yan, and X.-Y . Li,
"freeloc: Wireless-based cross-domain device-free fingerprints
localization to free user's motions,"IoT-J, vol. 11, no. 14, pp. 25
099--25 110, 2024.

\[209\] B. Zhou, R. Zhou, Y . Luo, and Y . Cheng, "Towards cross domain
csi action recognition through one-shot bimodal domain adaptation," in
MobiQuitous. Springer, 2022, pp. 290--309.

\[210\] F. Wang, J. Han, S. Zhang, X. He, and D. Huang, "Csi-net:
Unified human body characterization and pose recognition,"arXiv preprint
arXiv:1810.03064, 2018.

\[211\] B. Lan, F. Wang, L. Xia, F. Nai, S. Nie, H. Ding, and J. Han,
"Bullydetect: Detecting school physical bullying with wi-fi and deep
wavelet transformer,"IoT-J, 2024.

\[212\] H. He, X. Huan, J. Wang, Y . Luo, H. Hu, and J. An, "P3id: A
privacy- preserving person identification framework towards
multi-environments based on transfer learning,"IEEE TMC, pp. 1--16,
2024.

\[213\] H. Liu, L. Xi, W. Wang, F. Zhang, and Z. J. Haas, "Openfi:
Open-set wifi human sensing via virtual embedding confidence-aware,"IEEE
TNSE, pp. 1--12, 2024.

\[152\] D. Wang, J. Yang, W. Cui, L. Xie, and S. Sun, "Airfi: empowering
wifi-based passive human gesture recognition to unseen environment via
domain generalization,"IEEE TMC, vol. 23, no. 2, pp. 1156--1168, 2022.

\[214\] T. DeVries and G. W. Taylor, "Improved regularization of
convolutional neural networks with cutout,"arXiv preprint
arXiv:1708.04552, 2017.

\[215\] W. Hou and C. Wu, "Rfboost: Understanding and boosting deep wifi
sensing via physical data augmentation,"IMWUT, vol. 8, no. 2, pp. 1--26,
2024.

\[216\] S. Liu, Z. Chen, M. Wu, H. Wang, B. Xing, and L. Chen,
"Generalizing wireless cross-multiple-factor gesture recognition to
unseen domains," IEEE TMC, 2023.

\[156\] Y . Mao, Z. Guo, B. Sheng, L. Gui, and F. Xiao, "Wi-cro:
Wifi-based cross domain activity recognition via modified gan,"IEEE TVT,
2024.

\[217\] A. Virmani and M. Shahzad, "Position and orientation agnostic
gesture recognition using wifi," inMobiSys, 2017, pp. 252--264.

\[174\] C. Xiao, S. Chen, F. Zhou, and J. Wu, "Self-supervised few-shot
time-series segmentation for activity recognition,"IEEE TMC, vol. 22,
no. 11, pp. 6770--6783, 2022.

\[68\] R. Xiao, J. Liu, J. Han, and K. Ren, "Onefi: One-shot recognition
for unseen gesture via cots wifi," inSenSys, 2021, pp. 206--219.

\[92\] L. Zhao, R. Xiao, J. Liu, and J. Han, "One is enough: Enabling
one-shot device-free gesture recognition with cots wifi," inINFOCOM.
IEEE, 2024, pp. 1231--1240.

\[218\] S. Wang, L. Wang, and W. Liu, "Feature decoupling and
regeneration towards wifi-based human activity recognition,"Pattern
Recognition, vol. 153, p. 110480, 2024.


### Pseudo Labeling
\[75\] R. Zhou, Z. Gong, K. Tang, B. Zhou, and Y . Cheng, "Device-free
cross location activity recognition via semi-supervised deep
learning,"Neural Computing and Applications, vol. 34, no. 12, pp. 10
189--10 203, 2022.

\[96\] J. Chen, S. Bi, X.-H. Lin, and Z. Quan, "Lager: Label-free
domain- adaptive wireless gesture recognition via latent feature
alignment and augmentation,"IoT-J, vol. 11, no. 23, pp. 37 928--37 941,
2024.

\[219\] B.-B. Zhang, D. Zhang, Y . Li, Y . Hu, and Y . Chen,
"Unsupervised domain adaptation for rf-based gesture recognition,"IoT-J,
vol. 10, no. 23, pp. 21 026--21 038, 2023.

\[118\] L. Sheng, Y . Chen, S. Ning, S. Wang, B. Lian, and Z. Wei, "Da-
har: Dual adversarial network for environment-independent wifi human
activity recognition,"Pervasive and Mobile Computing, vol. 96,
p. 101850, 2023.

\[100\] B.-B. Zhang, D. Zhang, Y . Hu, and Y . Chen, "Unsupervised
domain adaptation for wifi gesture recognition," inWCNC. IEEE, 2023,
pp. 1--6.

## Stage 4: 🐁 Model Deployment

### Transfer Learning
\[70\] F. Wang, Y . Lv, M. Zhu, H. Ding, and J. Han, "Xrf55: A radio
frequency dataset for human indoor action analysis,"IMWUT, vol. 8, no.
1, pp. 1--34, 2024.

\[210\] F. Wang, J. Han, S. Zhang, X. He, and D. Huang, "Csi-net:
Unified human body characterization and pose recognition,"arXiv preprint
arXiv:1810.03064, 2018.

\[153\] X. Ding, T. Jiang, Y . Li, W. Xue, and Y . Zhong, "Device-free
location- independent human activity recognition using transfer learning
based on cnn," inICC Workshops. IEEE, 2020, pp. 1--6.

\[220\] Y .-S. Chen, Y .-C. Chang, and C.-Y . Li, "A semi-supervised
transfer learning with dynamic associate domain adaptation for human
activity recognition using wifi signals,"Sensors, vol. 21, no. 24,
p. 8475, 2021.

\[221\] J. K. Brinke and N. Meratnia, "Scaling activity recognition
using channel state information through convolutional neural networks
and transfer learning," inProceedings of the International Workshop on
Challenges in Artificial Intelligence and Machine Learning for Internet
of Things, 2019, pp. 56--62.

\[222\] Y . Fang, B. Sheng, H. Wang, and F. Xiao, "Witransfer: A
cross-scene transfer activity recognition system using wifi," inTURC,
2020, pp. 59--63.

\[223\] G. Yin, J. Zhang, G. Shen, and Y . Chen, "Fewsense, towards a
scalable and cross-domain wi-fi sensing system using few-shot
learning,"IEEE TMC, vol. 23, no. 1, pp. 453--468, 2022.

\[224\] L. Zheng, S. Bi, S. Wang, Z. Quan, X. Li, X. Lin, and H. Wang,
"Resmon: Domain-adaptive wireless respiration state monitoring via
few-shot bayesian deep learning,"IoT-J, vol. 10, no. 23, pp. 20 914-- 20
927, 2023.

\[225\] S. Bi, X. Chen, L. Zheng, H. Hou, and X. Lin, "Roger: Few-shot
learning based robust gesture recognition with multi-modal wi-fi csi
measurements," inICMLCN. IEEE, 2024, pp. 517--522.\[226\] H. Hou, S. Bi,
L. Zheng, X. Lin, and Z. Quan, "Sample-efficient cross- domain wifi
indoor crowd counting via few-shot learning," inWOCC. IEEE, 2022,
pp. 132--137.

\[227\] H. Hou, S. Bi, L. Zheng, X. Lin, Y . Wu, and Z. Quan,
"Dasecount: Domain-agnostic sample-efficient wireless indoor crowd
counting via few-shot learning,"IoT-J, vol. 10, no. 8, pp. 7038--7050,
2022.

### Federated Learning
\[228\] S. M. Hernandez and E. Bulut, "Wifederated: Scalable wifi
sensing using edge-based federated learning,"IoT-J, vol. 9, no. 14,
pp. 12 628-- 12 640, 2021.

\[229\] H. Geng, D. Deng, W. Zhang, P. Ji, and X. Wu, "Personalized
federated learning based on bidirectional knowledge distillation for
wifi gesture recognition,"Electronics, vol. 12, no. 24, p. 5016, 2023.

\[230\] X. Li, F. Song, M. Luo, K. Li, L. Chang, X. Chen, and Z. Wang,
"Towards collaborative and cross-domain wi-fi sensing: A case study for
human activity recognition,"IEEE TMC, vol. 23, no. 2, pp. 1674-- 1688,
2023.

\[231\] W. Qi, R. Zhang, J. Zhou, H. Zhang, Y . Xie, and X. Jing, "A
resource-efficient cross-domain sensing method for device-free gesture
recognition with federated transfer learning,"IEEE TGCN, vol. 7, no. 1,
pp. 393--400, 2023.

\[232\] S. Zhang, T. Jiang, X. Ding, Y . Zhong, and H. Jia, "A
cloud-edge col- laborative framework for cross-environment human action
recognition based on wi-fi," inIEEE/CIC ICC in China, 2023, pp. 1--6.

\[119\] L. Zhang, W. Cui, B. Li, Z. Chen, M. Wu, and T. S. Gee,
"Privacy- preserving cross-environment human activity recognition,"IEEE
Trans- actions on Cybernetics, vol. 53, no. 3, pp. 1765--1775, 2021.

\[233\] N. Zheng, Y . Li, S. Jiang, Y . Li, R. Yao, C. Dong, T. Chen, Y
. Yang, Z. Yin, and Y . Liu, "Adawifi, collaborative wifi sensing for
cross- environment adaptation,"IEEE TMC, pp. 1--15, 2024.

\[234\] J. Zhang, Y . Li, Q. Li, and W. Xiao, "Variance-constrained
local--global modeling for device-free localization under
uncertainties,"IEEE TII, 2023.



### Continual Learning
\[192\] B. Yang, H. Wang, L. Hu, H. Zhu, C.-T. Lam, and K. Fang,
"Few-shot cross-domain based wifi sensing system for online learning in
iot," IEEE Sensors Journal, 2023.

\[235\] Y . Bai, Z. Wang, K. Zheng, X. Wang, and J. Wang, "Widrive:
Adaptive wifi-based recognition of driver activity for real-time and
safe takeover," inICDCS. IEEE, 2019, pp. 901--911.

\[236\] E. Soltanaghaei, R. A. Sharma, Z. Wang, A. Chittilappilly, A.
Luong, E. Giler, K. Hall, S. Elias, and A. Rowe, "Robust and practical
wifi hu- man sensing using on-device learning with a domain adaptive
model," inProceedings of the ACM International Conference on Systems for
Energy-Efficient Buildings, Cities, and Transportation, 2020, pp. 150--
159.

\[237\] S. Zhai, Z. Tang, P. Nurmi, D. Fang, X. Chen, and Z. Wang,
"Rise: Robust wireless sensing using probabilistic and statistical
assessments," inMobiCom, 2021, pp. 309--322.

\[238\] Q. Fu, F. Wang, M. Zhu, H. Ding, J. Han, and T. X. Han, "Ccs:
Con- tinuous learning for customized incremental wireless sensing
services," arXiv preprint arXiv:2412.04821, 2024.

\[239\] T. Zhang, Q. Fu, H. Ding, G. Wang, and F. Wang, "Carec:
Continual wireless action recognition with expansion-compression
coordination," Sensors, 2025.

\[240\] Y . Zhang, F. He, Y . Wang, D. Wu, and G. Yu, "Csi-based cross-
scene human activity recognition with incremental learning,"Neural
Computing and Applications, vol. 35, no. 17, pp. 12 415--12 432, 2023.
