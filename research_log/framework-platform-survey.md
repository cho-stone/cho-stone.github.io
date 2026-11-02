# Survey of Research Tools, Frameworks, and Platforms for Autonomous Systems

## Objective

The goal of this survey is to identify suitable tools, frameworks, and platforms for future research and to refine potential research directions.

- Mobile Robotics
- Autonomous Driving
- Decision Making
- Reinforcement Learning
- Simulation


## Autonomous Driving

### CARLA

GitHub : https://github.com/carla-simulator/carla

**Type** : Autonomous driving simulator and research platform

**Purpose** : To develop, train, and evaluate autonomous driving systems in realistic and configurable virtual environments.

**Main Features**
- Flexible Python/C++ API for controlling the simulation
- Configurable vehicles, pedestrians, traffic, and weather
- Various autonomous-driving sensors
- Realistic urban driving environments
- Traffic scenario simulation
- Custom map support

**Simulation Environment** : Unreal Engine-based 3D simulation

**Supported Agents**
- Vehicles
- Pedestrians
- Ego vehicle
- NPC / background traffic vehicles

**Sensor Support**
- Cameras: RGB, Depth, Semantic / Instance Segmentation, Optical Flow
- LiDAR and Semantic LiDAR
- Radar
- GNSS
- IMU
- Collision, Lane Invasion, and Obstacle Sensors
- V2X Communication Sensors
- etc...

**Decision-Making Support**<br>
CARLA provides the environment, observations, vehicle control interface, traffic simulation, and scenario tools required for decision-making research.
We can implement their own decision-making methods using sensor or simulator state information and control vehicles through the Python API.

**Reinforcement Learning Support**<br>
CARLA can be used as an environment for reinforcement learning by defining:
- Observations from sensors or simulator states
- Actions such as steering, throttle, and braking
- Reward functions
- Episode termination conditions

However, CARLA itself is not an RL framework. RL algorithms and training pipelines generally need to be implemented using external libraries such as PyTorch, RLlib, Stable-Baselines3, or custom implementations.

**Multi-Agent Support**<br>
Multiple vehicles and pedestrians can exist and be controlled simultaneously.
CARLA therefore supports multi-agent experiments and interactive driving scenarios, but it does not provide a complete multi-agent reinforcement learning framework by itself.

**Integration with Other Tools**
- ROS 2
- Autoware
- ScenarioRunner
- OpenSCENARIO
- Scenic
- RoadRunner / OpenDRIVE
- CARLA Leaderboard

**Strengths**
- Realistic visual and physical simulation
- Rich sensor simulation
- Flexible Python API
- Strong for autonomous driving research
- Complex traffic and pedestrian interactions
- Suitable for perception, planning, decision-making, and end-to-end driving research

**Limitations**
- High computational requirements
- More complex setup than lightweight driving simulators
- Slower simulation and training throughput compared with lightweight RL-oriented simulators
- Reinforcement learning pipelines must generally be implemented separately
- Sim-to-real differences still exist despite realistic simulation

### SUMO

GitHub: https://github.com/eclipse-sumo/sumo

Type:

Purpose:

Main Features:

Traffic Simulation:

Supported Agents:

Vehicle Behavior:

Multi-Agent Support:

Traffic Control Support:

Integration with Other Simulators:

Strengths:

Limitations:

### MetaDrive

GitHub: https://github.com/metadriverse/metadrive

Type:

Purpose:

Main Features:

Simulation Environment:

Supported Agents:

Decision-Making Support:

Reinforcement Learning Support:

Multi-Agent Support:

Strengths:

Limitations:

Comparison with CARLA:

### SMARTS

GitHub: https://github.com/huawei-noah/SMARTS

Type:

Purpose:

Main Features:

Simulation Environment:

Supported Agents:

Decision-Making Support:

Reinforcement Learning Support:

Multi-Agent Support:

Strengths:

Limitations:

Comparison with CARLA / MetaDrive:

## Mobile Robotics

### Nav2

GitHub: https://github.com/ros-navigation/navigation2

Type:

Purpose:

Main Components:

Navigation Architecture:

Global Planning:

Local Planning / Control:

Decision-Making Related Components:

Simulation Integration:

ROS 2 Integration:

Strengths:

Limitations:

### Nav2SocialRL

GitHub: https://github.com/maxijsseldijk/Nav2SocialRL

Type:

Based On:

Purpose:

Simulation Environment:

Dynamic Agents:

Observation:

Action:

Learning Method:

Decision-Making Level:

Nav2 Integration:

Strengths:

Limitations:

## Perception and Human Understanding

### YOLO

GitHub: https://github.com/ultralytics/ultralytics

Type:

Purpose:

Main Features:

Input:

Output:

Object Detection Support:

Tracking Support:

Potential Role in Autonomous Driving:

Potential Role in Mobile Robotics:

Potential Role in Decision Making:

Strengths:

Limitations:

### OpenPose

GitHub: https://github.com/CMU-Perceptual-Computing-Lab/openpose

Type:

Purpose:

Main Features:

Input:

Output:

Human Pose Information:

Multi-Person Support:

Potential Role in Autonomous Driving:

Potential Role in Mobile Robotics:

Potential Role in Human-Aware Decision Making:

Strengths:

Limitations:

## My Thoughts

Coming soon.

## Next Steps

Coming soon.
