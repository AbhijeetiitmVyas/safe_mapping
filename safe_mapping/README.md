# active-safe-mapping
ROS package for simulating UAV landing area exploration with visual sensing. Implements novel reinforcement-based active learning paradigm. Requires ROS, Gym, Ray.

The safe mapping problem for UAV landing is defined as follows: given an unknown area, create an (x, y)-map of where it is safe to land and
where it is not. In the current setting the agent has access to the labels only through a process called probing, i.e,  the agent needs to visit the the location to obtain the ground truth label. Our goal is to use visual information to both create this model and plan the flight trajectory. An inbuilt PI controller is used to fly the drone and the learning process is only on the trajectory level. In our main approach, 
the underlying safe-mapper model is a LSTM-CNN which learns from labeled data collected by sampling from the environment according
to the decisions of an RL agent which gets rewards from the improvement of the safe-mapper model. This package includes the algorithm
implementation and tools for testing, especially in Gazebo simulation.
