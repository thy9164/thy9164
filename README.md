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
