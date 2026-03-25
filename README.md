# RMIL Teleoperation Project (Falcon → Franka Panda)

Course project: teleoperate a Franka Panda robot arm using a **Novint Falcon haptic device**.

## Overview

- **Leader**: reads Falcon haptic input and publishes teleoperation commands.
- **Follower**: controls the robot using a **`cartesian_impedance_controller`**.

## Run

In separate terminals on the corresponding machines/workspaces:

- **Follower**

```bash
roslaunch franka_teleop_lmt Teleop.launch robot_ip:=
```

- **Leader**

```bash
roslaunch franka_teleop_lmt Teleop_final_project.launch
```

## Notes

- Make sure both sides are on the same ROS network (e.g. `ROS_MASTER_URI`, `ROS_IP/ROS_HOSTNAME`).
- `robot_ip` should be set to the Panda controller IP on the follower side.
