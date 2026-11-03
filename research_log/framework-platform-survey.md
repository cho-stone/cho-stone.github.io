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

**Type:** Open source robotics software framework and development platform

**Purpose:** To provide a common software infrastructure for developing robot systems by connecting sensors, algorithms, controllers, and hardware through standardized communication interfaces.

**Role in Mobile Robotics:** software backbone connecting different components of a mobile robot.

**Communication Architecture:** ROS 2 uses a distributed node-based architecture where different robot components communicate through Topics, Services, and Actions.

**Sensor Integration**
- LiDAR
- RGB / Depth Camera
- IMU
- Wheel Encoders
- GNSS
- etc...

**Robot Control:** ROS 2 can connect high-level algorithms to robot hardware.

**Simulation Integration**
ROS 2 can be integrated with robotics simulators such as:
- Gazebo
- NVIDIA Isaac Sim

This allows the same ROS 2-based software architecture to be tested first in simulation and later connected to a real robot.

**Nav2 Integration**
Nav2 is a navigation framework built for ROS 2.

ROS 2 provides the communication infrastructure while Nav2 provides navigation-related components such as:
- Localization
- Costmaps
- Global Planning
- Local Planning / Control
- Behavior Trees
- Recovery Behaviors

**Real Robot Integration**
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

**Environment Customization:**

**Strengths:**

**Limitations:**

**My Thoughts**<br>

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

## Learning-Based and Social Navigation Frameworks

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

Keeping survey
