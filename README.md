<img width="432" height="86" alt="image" src="https://github.com/user-attachments/assets/0be73a90-01bd-456e-b774-ae877fe9a7a0" /><img width="432" height="86" alt="image" src="https://github.com/user-attachments/assets/5c4ef84e-7485-4152-97d4-2e4c2e59db9a" />

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Abstract

The **NCBD (NanNing Normal University Classroom Behavior Datasets)** is a large-scale, high-quality video dataset specifically designed for student classroom behavior recognition in open-environment settings. This dataset aims to address the scarcity of specialized datasets in the field of classroom behavior analysis, providing a solid foundation for the training and evaluation of related algorithms.

The construction of NCBD acknowledges and addresses numerous challenges inherent to real-world classroom environments. These challenges include the unstructured nature of video data, significant class imbalance among behaviors, complex environmental factors (e.g., varying illumination, occlusions), semantic ambiguity of certain actions, and the critical sensitivity of student privacy. By employing a non-intrusive, concomitant data collection method in authentic educational settings and adhering to a rigorous annotation protocol, NCBD paves the way for developing more robust and accurate classroom behavior recognition models.

## Dataset Details

### Data Collection
* **Location**: Authentic classrooms at a normal university in Southwest China.
* **Participants**: The dataset covers a diverse student population, including undergraduate and graduate students from various majors and class levels.
* **Equipment**: A Xiaomi 2K resolution pan-tilt-zoom (PTZ) camera was used for recording.
* **Methodology**: A non-intrusive, concomitant data collection approach was adopted. The camera was typically placed at the front of the classroom (e.g., above the blackboard) to capture the natural behavior of students.
* **Timeline**: The raw video footage was recorded in August 2022, and the complete annotation process was finalized by the end of the same year.
* **Ethics & Privacy**: This project places a high priority on ethical considerations and privacy protection. All video recordings were conducted **only after obtaining prior informed consent from both the course instructor and all attending students**. Necessary data anonymization measures have been implemented.


### Behavior Categories

The dataset defines **nine** common types of student classroom behaviors:

|                    |                  |                       |
| :----------------- | :--------------- | :-------------------- |
| 1. Listen (听讲)   | 4. Write (写字)  | 7. Use Phone (使用手机) |
| 2. Read (看书)     | 5. Yawn (打哈欠) | 8. Use Computer (使用电脑) |
| 3. Turn Head (转头) | 6. Eat (吃东西)  | 9. Drink (喝水)         |

<p align="center">
  <img src="https://github.com/kuangxiaoye/NCBD/blob/main/BehaviorClassifications.png" width="600" alt="Behavior Categories Visualization">
  <br>
  <em>Figure 1: The nine behavior categories defined in the NCBD dataset.</em>
</p>

### Dataset Statistics
* **Total Samples**: The dataset contains **1,024** curated video clips of student behaviors.
* **Data Split**: The dataset is partitioned into training, validation, and test sets following a strict 3:1:1 ratio.
    * **Training Set**: 614 clips
    * **Validation Set**: 205 clips
    * **Test Set**: 205 clips

<p align="center">
  <img src="https://github.com/kuangxiaoye/NCBD/blob/main/Distribution.png" width="500" alt="Dataset Split Chart">
  <br>
  <em>Figure 2: Sample distribution of the NCBD dataset.</em>
</p>

### Annotation Process

To ensure high-quality annotations and efficiency, a **semi-automated annotation workflow** was implemented:
1.  **Initial Recognition**: An I3D network, pre-trained on the Kinetics-400 dataset, was used to perform preliminary feature recognition and classification on the raw video footage.
2.  **Manual Verification**: Researchers meticulously reviewed and calibrated each machine-labeled clip. This human-in-the-loop process ensured the absolute accuracy of the start/end times and the behavior label for every sample.
3.  **Data Cleaning**: The final dataset was refined by removing duplicate or noisy samples, resulting in a high-quality collection of behavior clips.

Each video clip is trimmed to a duration of 1 to 10 seconds to capture a complete and distinct behavioral unit.

## Data Access and Privacy Agreement

In strict adherence to student privacy protection and to ensure the responsible use of our data, **the raw video files of this dataset are not publicly available**. We only share **extracted feature data**. This approach preserves the essential behavioral information for research while anonymizing student identities.

To request access to the feature data, you must:
1.  Clearly state your research purpose.
2.  Agree to and sign a data usage and privacy protection agreement. This agreement mandates that the data will be used solely for non-commercial academic research, that no attempt will be made to re-identify individuals, and that the data will be stored securely.

**Please initiate the application process by contacting us via email at [w258765@gmail.com](mailto:w258765@gmail.com).**

## Citation

If you use the NCBD dataset in your research, please cite our work:

```bibtex
@phdthesis{Wang_NCBD_2024,
  author  = {Ye, Wang},
  title   = {{Research and application of student classroom behavior recognition in an open environment}},
  school  = {NanNing Normal University},
  year    = {2024},
  note    = {Original title: 开放环境下的学生课堂行为识别研究及应用}
}
