# Survey of Tools and Frameworks for Mobile Robot Research

## Objective

The goal of this survey is to identify suitable tools and frameworks for developing mobile robot algorithms, evaluating them in simulation, and validating them in real-world environments.

The main research interests are:

- Mobile Robotics
- Navigation
- Decision Making
- Dynamic Environments
- Reinforcement Learning
- Simulation
- Sim-to-Real Validation

## Core Infrastructure

### ROS 2

Official Website: https://www.ros.org/

**Type :** Open source robotics software framework and development platform

**Purpose :** To provide a common software infrastructure for developing robot systems by connecting sensors, algorithms, controllers, and hardware through standardized communication interfaces.

**Role in Mobile Robotics :** software backbone connecting different components of a mobile robot.

**Communication Architecture :** ROS 2 uses a distributed node-based architecture where different robot components communicate through Topics, Services, and Actions.

**Sensor Integration**
- LiDAR
- RGB / Depth Camera
- IMU
- Wheel Encoders
- GNSS
- etc...

**Robot Control :** ROS 2 can connect high-level algorithms to robot hardware.

**Simulation Integration**<br>
ROS 2 can be integrated with robotics simulators such as:
- Gazebo
- NVIDIA Isaac Sim

This allows the same ROS 2-based software architecture to be tested first in simulation and later connected to a real robot.

**Nav2 Integration**<br>
Nav2 is a navigation framework built for ROS 2.

ROS 2 provides the communication infrastructure while Nav2 provides navigation-related components such as:
- Localization
- Costmaps
- Global Planning
- Local Planning / Control
- Behavior Trees
- Recovery Behaviors

**Real Robot Integration**<br>
The same ROS 2 nodes used in simulation can often be reused on a real robot if the simulated and real hardware provide compatible interfaces.
This makes ROS 2 suitable for simulation-to-real-world research.

**Strengths**
- Modular and distributed architecture
- Strong robotics ecosystem
- Supports Python and C++
- Integration with many sensors and robot platforms
- Strong support for simulation

**Limitations**
- Relatively steep learning curve
- Large ecosystem can be complex
- Configuration and debugging can become difficult in large systems
- Real robot integration still requires hardware-specific drivers and configuration

**My Thoughts**<br>
Using ROS 2 would make it possible to develop and evaluate an algorithm in simulation and later transfer the same software architecture to a real mobile robot.

## Simulation Platforms

### Gazebo

GitHub: https://github.com/gazebosim/gz-sim

**Type:** Open-source robotics simulator

**Purpose:** To simulate robots, sensors, physical interactions, and environments for robot development and testing before deployment on real hardware.

**Main Features**
- 3D robot simulation
- Physics simulation
- Sensor simulation
- Custom robot and environment models
- Plugin-based extensibility
- Graphical simulation interface
- ROS 2 integration
- Support for mobile robot simulation

**Physics Simulation**<br>
Gazebo provides physics simulation for robot motion, collisions, contacts, joints, and interactions with the environment.<br>
It can use multiple physics engines through the Gazebo Physics interface.

**Supported Robots**
- Differential-drive mobile robots
- Wheeled robots
- Manipulators
- Drones
- Legged robots
- Custom robot models

**Sensor Support**
- LiDAR
- Camera
- Depth Camera
- IMU
- GPS / GNSS
- Contact Sensor
- Force / Torque Sensor
- etc...

**Dynamic Agents**<br>
Gazebo can simulate multiple moving robots and dynamic objects in the same environment.<br>
Custom plugins, scripts, or external ROS 2 nodes can be used to control other robots or moving agents.<br>
However, realistic pedestrian or social behavior is not provided as a complete built-in social navigation system and may require additional models or frameworks.

**ROS 2 Integration**<br>
Gazebo can communicate with ROS 2 using the ros_gz integration packages.<br>
The ros_gz_bridge allows information to be exchanged between Gazebo and ROS 2, including:
- Sensor data
- Joint states
- Robot commands
- Transform information
- Simulation data

**Nav2 Integration**<br>
Gazebo can be used together with Nav2 to test mobile robot navigation.
- Robot model
- Odometry
- LiDAR / Depth Camera
- Localization
- Costmaps
- Global Planner
- Local Controller

This makes it possible to test Nav2-based navigation before deploying the system on a real robot.

**Reinforcement Learning Support**<br>
Gazebo can be used as a simulation environment for reinforcement learning.<br>
However, Gazebo itself is not a reinforcement learning framework.<br>
Researchers generally need to implement or connect:
- Observation definitions
- Action spaces
- Reward functions
- Episode reset logic
- RL algorithms and training pipelines

using external frameworks such as PyTorch, Stable-Baselines3, RLlib, or custom implementations.

**Environment Customization**
- Robot models
- Buildings and rooms
- Obstacles
- Dynamic objects
- Sensor configurations
- Physical properties

**Strengths**
- Strong integration with ROS 2
- Suitable for mobile robot research
- Supports realistic robot physics and sensors
- Highly customizable
- Works well with Nav2
- Can simulate the same sensor interfaces used by a real robot
- Open-source and widely used in robotics research

**Limitations**
- Simulation setup can be complex
- Robot and sensor models require configuration
- Realistic human behavior is not provided by default
- Reinforcement learning pipelines must be implemented separately
- Physics and sensor behavior cannot perfectly reproduce the real world

**My Thoughts**<br>
Gazebo could be used as the main simulation environment for developing and evaluating mobile robot navigation and decision-making algorithms.<br>
A possible structure is:

```text
Gazebo
   ↓
Simulated LiDAR / Depth Camera / Odometry
   ↓
ROS 2
   ↓
Nav2 / Proposed Algorithm
   ↓
Robot Command
```
Gazebo is suitable for simulation-to-real-world research because simulated and real robots can use similar ROS 2 interfaces.<br>
The proposed algorithm should therefore use observations that can also be obtained or estimated from real sensors.

### NVIDIA Isaac Sim

Official Website: https://developer.nvidia.com/isaac/sim

**Type:**

**Purpose:**

**Main Features:**

**Physics Simulation:**

**Supported Robots:**

**Sensor Support:**

**Dynamic Agents:**

**ROS 2 Integration:**

**Nav2 Integration:**

**Reinforcement Learning Support:**

**Synthetic Data Support:**

**Strengths:**

**Limitations:**

**My Thoughts**<br>

## Navigation Framework

### Nav2

GitHub: https://github.com/ros-navigation/navigation2

**Type:**

**Purpose:**

**Main Components:**

**Navigation Architecture:**

**Localization / State Estimation:**

**Environmental Representation / Costmap:**

**Global Planning:**

**Local Planning / Control:**

**Behavior Trees:**

**Obstacle Avoidance:**

**Sensor Integration:**

**Simulation Integration:**

**ROS 2 Integration:**

**Custom Algorithm Integration:**

**Strengths:**

**Limitations:**

**My Thoughts**<br>

### Nav2SocialRL

GitHub: https://github.com/maxijsseldijk/Nav2SocialRL

**Type:**

**Based On:**

**Purpose:**

**Simulation Environment:**

**Dynamic Agents:**

**Observation:**

**Action:**

**Learning Method:**

**Decision-Making Level:**

**Social Navigation Support:**

**Nav2 Integration:**

**Gazebo Integration:**

**Strengths:**

**Limitations:**

**My Thoughts**<br>

## Next Steps

Surveying Recent Research Trends
