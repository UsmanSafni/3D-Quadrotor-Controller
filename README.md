# 3D-Quadrotor-Controller

## Introduction
This repository contains the code for a 3D Quadrotor Controller and Trajectory Generation system. The project involves the creation of a Proportional-Derivative (PD) controller to control a quadrotor in three dimensions. Additionally, it includes a trajectory generation module to guide the quadrotor through a series of waypoints in a time-parameterized manner.

## System Model
The quadrotor is modeled using a combination of coordinate systems, motor models, and rigid body dynamics. The controller relies on linearized equations of motion derived from a nominal hover state, and the trajectory generation is based on minimum snap trajectories.

## Components

1. **Controller**
   - The `controller.m` file contains the implementation of the PD controller. It takes sensor readings, calculates errors, and determines the necessary inputs (thrust and moments) to control the quadrotor's position and attitude.

2. **Trajectory Generation**
   - The `traj_generator.m` file is responsible for generating trajectories through a set of waypoints. It utilizes minimum snap trajectory principles, ensuring smooth transitions between waypoints while considering quadrotor dynamics.

3. **Simulation**
   - The `runsim.m` script serves as a test script, allowing users to observe the quadrotor's behavior under different trajectory scenarios. It calls the `simulation_3d.m` file to run the simulation.

4. **Evaluation**
   - The `evaluate.m` script evaluates the performance of the controller on predefined trajectories. It calculates position errors and provides feedback on how well the quadrotor follows the specified paths.

5. **Trajectory Examples**
   - Two pre-defined trajectories, `traj_helix.p` and `traj_line.p`, showcase different scenarios for testing the controller's capabilities.


