# 112-2 Computer Vision Midterm Proposal

## Title and Authors

#### Driving Monitor System base on Yolov7
陳禹勳 312581014  廖永誠 312581029
## 4 sections:

### Sec 1. Intro: problem you want to solve and why

In recent years, traffic accidents have become increasingly common, with driver fatigue and distraction being among the primary causes. To effectively reduce the occurrence of traffic accidents and improve road safety, it is crucial and urgent to develop a Driver Monitoring System (DMS).

The primary objective of a DMS is to monitor the driver's condition in real-time, promptly detecting dangerous driving behaviors such as fatigue and distraction. Upon detection, the system provides appropriate alerts to remind the driver to maintain focus and alertness, thereby preventing traffic accidents. A DMS can employ various technological approaches, such as:

1. Image recognition: Capturing the driver's facial expressions, eye movements, and other cues through an in-vehicle camera to determine if the driver is fatigued or distracted.
2. Physiological signal monitoring: Collecting the driver's physiological signals, such as heartbeat and breathing, using sensors to analyze their mental state.
3. Behavior analysis: Inferring the driver's risk level based on their operating behaviors, such as sudden acceleration or sharp turns.
    
By implementing a DMS, we can significantly enhance road safety, reduce traffic accidents caused by human factors, and protect the lives and property of drivers and passengers. Additionally, a DMS can provide valuable data and insights for insurance companies, fleet management, and other related industries, promoting industry development and innovation.

In recent years, due to the continuous advancements in YOLO (You Only Look Once) image recognition, it has become possible to identify objects in real-time at very high speeds. This progress also enables us to implement real-time applications using YOLO, including DMS systems.

In summary, utilizing YOLO object detection technology to develop DMS not only contributes to improving traffic safety but also has broad market prospects and application value, making it worthy of our investment in research and implementation.
    
### Sec 2. Technical part: how do you propose to solve it?

#### High Level System Architecture

- High level system architecture diagram for the Driver Monitoring System (DMS) using YOLO object detection:
    ![image](https://hackmd.io/_uploads/H1sNo1g10.png)

#### System Components Implementation

1. State Recognition (YOLO)
    The state recognition component using YOLO object detection focuses on identifying the state of the driving environment by detecting and classifying various objects and their states. This includes:

    Detecting the driver's facial features, such as eyes, and determining their state (e.g., eyes closed or open) to assess the driver's alertness level.
    Identifying the presence and state of objects like seat belts (fastened or unfastened), phones (in use or not), and the driver's head position to determine if the driver is distracted or not following safety guidelines.
    
2. Post Processing

    The post-processing component takes the objects and their states identified by the State Recognition (YOLO) component and combines them to form meaningful features. These features represent specific patterns or combinations of objects and states that can be used to infer the driver's current condition.

    By developing a set of logical rules or algorithms, the post-processing component determines how different combinations of features correspond to various driver states. For example:

    1. If the phone object is detected in close proximity to the driver's head object for a specified duration (e.g., `X` seconds), the system may conclude that the driver is in the "Using Phone" state, indicating a distraction.
    
    2. If the driver's eyes are detected as closed for more than a certain period (e.g., `X` seconds), the system may infer that the driver is in the "Sleeping" state, suggesting fatigue or drowsiness.
    
    Following is `High Level Diagram`

    ![螢幕擷取畫面 2024-03-26 143410](https://hackmd.io/_uploads/BJzK21gJC.png)
    
### Sec 3, 4. Milestones achieved so far & Remaining milestones (dates and sub-goals)

![甘特圖](https://hackmd.io/_uploads/S1NsUgx1A.png)

Based on our project proposal for developing a Driver Monitoring System using Yolov7, here's a description of our milestone planning:

The project starts on March 26, 2024, and ends on June 3, 2024. It is divided into several tasks that will be completed over 68 days.

From March 26 to April 7, we will spend 12 days writing the project proposal and surveying papers related to Yolov7, which will be used for state recognition in the Driver Monitoring System.

Between April 8 and April 20, we will spend 12 days becoming familiar with how to use Yolov7 and collecting the necessary dataset for training the model. The dataset will include images or videos of drivers in various states, such as distracted, fatigued, or alert.

From April 15 to May 1, we will spend 16 days training the Yolov7 model using the collected dataset. This will involve fine-tuning the model's parameters to accurately detect and classify driver states based on facial features and object detection.

In the next phase, from May 2 to May 20, we will spend 17 days writing the post-processing code. The post-processing component will combine the detected objects and states from the Yolov7 model to infer the driver's condition based on predefined rules or algorithms. We will also conduct preliminary tests to ensure the system is working as intended.

From May 21 to May 31, we will spend 9 days fine-tuning the implementation plan based on insights gained from the preliminary tests. We will make necessary adjustments to improve the system's performance and create a final plan for completing the project.

Finally, from June 1 to June 3, we will spend 2 days compiling the final results of the Driver Monitoring System, which will include the trained Yolov7 model, post-processing component, and overall system performance metrics.

## References

1. [YOLOv7 Paper](https://arxiv.org/abs/2207.02696)
2. [YOLOv7 Source Code](https://github.com/WongKinYiu/yolov7)
3. [Driver Monitoring System](https://en.wikipedia.org/wiki/Driver_monitoring_system)
