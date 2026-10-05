# Hung-Yao Tsai

Computer Science and Information Engineering graduate from National Cheng Kung University (NCKU), with interests in computer vision and machine learning, especially for baseball and sports video analysis. My projects have explored pose-based pitching analysis and temporal refinement of bat keypoint detection. I am also interested in broader computer vision, machine learning, and software engineering work.

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
     width="900">

- **Built a pitching motion analysis system for ordinary side-view videos**
  - Used MediaPipe Pose to extract 2D body landmarks and motion features

- **Designed logic to estimate three key pitching events**
  - **Foot Contact:** used lead-foot motion, velocity, and landing behavior
  - **Maximum External Rotation:** used 2D throwing-forearm orientation as a timing proxy
  - **Ball Release:** estimated release timing from arm geometry without detecting the ball

- **Added motion-analysis features and an interactive review interface**
  - Visualized lead-knee angle and extension, hip-center trajectory, and pitching phases
  - Supported frame-by-frame review and direct navigation to detected pitching events

- **Evaluated the event-estimation logic on six pitching clips**
  - Foot Contact: predictions in **4 of 6 clips** fell within the frames manually annotated as first contact
  - MER and Ball Release: in all **6 clips**, predictions fell within the manually annotated frame range or **1 frame outside it**
  - Results are based on only six clips, so this should be viewed as a small-scale evaluation

*Two-person undergraduate project; I independently developed the pitching-analysis system shown here, while my teammate developed a separate batting-analysis system.*

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
