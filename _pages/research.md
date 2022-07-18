---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
redirect_from:
  - /research
---

My research focuses on developing techniques to guarantee the safety of autonomous aerial vehicles moving under unforeseen conditions such as disturbances, intermittent sensing, model changes and failures.

Meta-learning-based Trajectory Tracking under Unforeseen Faults
====

<img src="../images/iros2021-intro.svg"
     alt="Trajectory adaptation"
     caption="© 2021 IEEE"
     width="400" 
     height="480"
     style="float: right;" />

An autonomous robot may experience unforeseen faults during real-world operations which may affect its safety and intended behavior. To deal with this problem, we propose a meta-learning-based approach to improve the trajectory tracking performance of an unmanned aerial vehicle (UAV) under actuator faults which have not been previously experienced. Meta-learning is leveraged to train a model that is easily adaptable at runtime to make accurate predictions about the system’s future state. A runtime monitoring and validation technique is proposed to decide when the system needs to adapt its model by considering a data pruning procedure for efficient learning. Finally, the reference trajectory is adapted based on future predictions by borrowing feedback control logic to make the system track the original and desired path without needing to access the system’s controller. More details, simulation and experimental results can be found in the paper: [IROS'21](https://ieeexplore.ieee.org/document/9635918 "IROS'21").

Runtime Planning, Learning, and Recovery under Unforeseen Disturbances
====

<img src="../images/payload.png"
     alt="Assured planning"
     width="400" 
     height="480"
     style="float: right;" />

Autonomous systems are typically designed and trained to work under certain system and environmental conditions. However, in real-world applications, the system may face unexpected situations such as component failures, variation in payload distribution or changes in model dynamics at runtime. Such factors could lead the system to undesired conditions if they are not properly taken into consideration. 

To provide safety under unforeseen distrurbances at runtime,  a fast online planning, learning, and recovery approach is introduced. By leveraging Gaussian Process regression theory in which a model is continuously trained and adapted using data collected during the autonomous operation, the disturbance and its effects are predicted at runtime to plan safe trajectories. This approach is validated on simulations and experiments on a UAV carrying an unknown payload outside of the training bounds.  More details, simulation and experimental results can be found in the paper: [IROS'20](https://ieeexplore.ieee.org/document/9341641 "IROS'20").

Assured Runtime Monitoring and Planning
====

<img src="../images/assured_planning.png"
     alt="Assured planning"
     width="400" 
     height="480"
     style="float: right; margin-left: 2px" />
Uncertain environments with the presence of disturbances and noises may lead the autonomous systems to reach unsafe states (e.g., collisions with obstacles) even while using well-tuned and precise controllers. Reachability analysis tools are very powerful to predict the future states of the system and provide safety guarantees, however they are challenging to use at runtime due to their computational complexity. Instead, we propose to use neural networks (NNs) to imitate the safety decisions of reachability tools by training the networks at the design time using reachability tools. The decisions of the neural network are used to replan trajectories when necessary. To guarantee that the NNs will make conservative safety decisions, they are verified using a closed-loop verification tool, Verisig. Verification results are also leveraged to retrain networks accordingly.  With this approach, the reachable set computation is limited to the offline stage, and safety-assured trajectories are designed at runtime in both known and unknown environments. More details, simulation and experimental results can be found in the article: [RAM '20](https://ieeexplore.ieee.org/document/9068251 "RAM'20").


GP-based Fast Runtime Monitoring and Recovery
====

<img src="../images/runtime_monitoring.png"
     alt="Runtime monitoring"
     width="400" 
     height="480"
     style="float: right; margin-left: 2px" />

Traditional unmanned aerial vehicle applications rely on constant sensor measurements for localization. However, in real-world applications, these sensor measurements can be interrupted due to various reasons such as sensor failures, signal occlusions, and communication problems (e.g., losing GPS signal while moving in a city around tall buildings). 

To guarantee the safety of the UAVs under intermittent sensing, we introduce a novel fast reachability approach which leverages Gaussian process regression to predict the future deviations at runtime. These reachable sets are then utilized to schedule when the system needs to monitor, replan its trajectories and perform recovery to continue safe operations. More details can be found in the paper: [IROS'19](https://ieeexplore.ieee.org/document/8968498 "IROS'19").


Reachability-based Self/Event-triggered Scheduling and Replanning
====

<img src="../images/scheduling.png"
     alt="Self-triggered scheduling"
     width="400" 
     height="480"
     style="float: right; margin-left: 2px" />

High-frequency  periodic sensor measurements are usually expected for a traditional system to safely navigate in environments occupied with obstacles. However, monitoring the sensors and processing the sensor measurements at high-frequency are computationally consuming, and often not necessary especially when the vehicle is operating in obstacle-free environments.

To minimize the computation associated with the sensor monitoring while guaranteeing safety, reachability analysis is leveraged to capture the future states of a UAV operating
under the effects of noise and disturbances in both static and dynamic environments under external disturbances and noises. 
Self-triggered scheduling is then utilized to compute when the system needs to perform sensor monitoring. More details about the approach and the simulation and experiment results can be found in our papers: [AHS'17](https://ieeexplore.ieee.org/document/8046382 "AHS'17") [ICRA'18](https://ieeexplore.ieee.org/document/8463205 "ICRA'18") [JINT'20](https://link.springer.com/epdf/10.1007/s10846-020-01192-2?sharing_token=qFtm8fdhrw7rGoxGSkag9Pe4RwlQNchNByi7wbcMAY7a0qUIrsI7Gsc1PxE0C73W76eRLdTfLaDkqH1k2r_lFJDR2pmTLZvq7Px2rnuCcKWhnHiTmHhqX_j3X_xVtcUXJzzrkbBCBQCbOpqqYUGu44c7CmLWpuWDkN5dZ2i4Jfk%3D "JINT '20")




