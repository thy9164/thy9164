# Hung-Yao Tsai

Computer Science and Information Engineering graduate from National Cheng Kung University (NCKU), with interests in computer vision and machine learning, especially for baseball and sports video analysis. My projects have explored pose-based pitching analysis and temporal refinement of bat keypoint detection. I am also interested in broader computer vision, machine learning, and software engineering problems.

## Selected Projects
### Baseball Bat Keypoint Detection and Temporal Refinement

<img src="https://raw.githubusercontent.com/thy9164/baseball-bat-temporal-refinement/main/docs/demo_assets/swing074_detector_vs_temporal.gif"
     alt="Frame-wise detector vs. temporal refinement"
     width="800">

- **Built a baseball bat keypoint detection and temporal-refinement pipeline**
  - Used YOLOv8-pose to detect bat head and tail keypoints
  - Used a 31-frame BiGRU to refine frame-wise keypoint predictions

- **Generated synthetic training data from 3D baseball swing motion data**
  - Projected 3D bat trajectories into 2D views
  - Added noise and missing keypoints to simulate detector errors and missed detections during pretraining

- **Reduced tail localization error on test swing videos**
  - Reduced RMSE from **19.956 px to 17.278 px (13.42%)** on 15 test swings
  - Most of the improvement came from frames with large detector errors; the temporal refiner was not consistently better on every frame.

*Completed as a two-person course project; the bullets above summarizes my contributions.*

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
