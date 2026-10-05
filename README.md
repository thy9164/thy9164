# Hung-Yao Tsai

Computer Science graduate from National Cheng Kung University (NCKU), interested in computer vision and machine learning for baseball and sports applications. I enjoy building practical systems from video data, from pose-based motion analysis to temporal refinement of visual detections, while remaining open to broader CV/ML and software engineering work.

## Selected Projects
### Baseball Bat Keypoint Detection and Temporal Refinement

<img src="https://raw.githubusercontent.com/thy9164/baseball-bat-temporal-refinement/main/docs/demo_assets/swing074_detector_vs_temporal.gif"
     alt="Frame-wise detector vs. temporal refinement"
     width="800">

A two-person course project on baseball bat endpoint localization, focusing on unstable frame-wise detections during fast swings.

**My work:** YOLO-based detection, dataset preparation and splits, synthetic 3D-to-2D training data, BiGRU temporal refinement, RAFT integration, and experiment analysis. I later audited and rebuilt the feature pipeline so that the temporal model used only information available at inference time.

**Result:** On 15 held-out test swings, the no-flow temporal refiner reduced tail RMSE from **19.956 px to 17.278 px (13.42%)**. Most of the improvement came from correcting large detector errors; adding RAFT reduced RMSE only slightly further to **17.177 px**.

**Limitation:** Refinement did not improve every frame, and the results do not support an occlusion-specific solution.

[View the project on GitHub →](https://github.com/thy9164/baseball-bat-temporal-refinement)

---

### Pitcher Motion Analysis

<img src="https://raw.githubusercontent.com/thy9164/pitcher-motion-analysis/main/assets/pitch_analysis_demo.gif"
     alt="Pitcher Motion Analysis demo"
     width="800">

An undergraduate project for analyzing baseball pitching motion from ordinary side-view video. The original project was completed by a two-person team; I independently developed the pitching-analysis system shown here, while my teammate built a separate batting-analysis system.

**What I built:** A MediaPipe Pose–based pipeline that detects three pitching events — **Foot Contact, Maximum External Rotation, and Ball Release** — using 2D landmark motion, joint geometry, and rule-based logic. I also added lead-knee analysis, hip-center trajectory visualization, pitching-phase segmentation, and a PyQt GUI for reviewing the detected events and motion features.

**Validation:** In a later evaluation on six additional pitching clips, **4/6 Foot Contact predictions** fell inside the annotated first-contact range. For **MER and Ball Release, all 6 predictions** were either inside the annotated range or within one frame of the nearest boundary.

**Limitation:** The method relies on monocular 2D pose estimates. MER is a timing proxy rather than a direct measurement of shoulder external rotation, and Ball Release is inferred from arm geometry rather than direct ball tracking.

[View the project on GitHub →](https://github.com/thy9164/pitcher-motion-analysis)

<!--
**thy9164/thy9164** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
