# ROS Packages for Task Constrained Mobile Manipulation Planning

This repository primarily contains an efficient sampling-based planning framework, called BI<sup>2</sup>RRT\*, that extends the Informed RRT\* of [Gammell et al.] towards bidirectional search, informed sampling for omnidirectional mobile manipulator robotic platforms and satisfaction of arbitrary geometric endeffector task constraints. The associated paper of the framework presented at the IEEE/RSJ International Conference on Intelligent Robots and Systems can be found in [Burget et al.]

Use the "*robot_motion.rosinstall*" file for downloading the ROS packages for robot [motion planning], [control] and [trajectory execution] distributed to different repositories:
- `robot_motion_planning`: Motion Planning using different RRT-based planning algorithms (including the novel BI<sup>2</sup>RRT\* planning framework)
- `robot_motion_control`: Jacobian-based motion control algorithms (Jacobian damped-least squares etc.)
- `robot_motion_execution`: Algorithms for executing the planned motion trajectories on a simulated and real robot platform

### Installation 

Create your workspace:
```sh
mkdir -p ~/my-ws/src
```

Copy the contents of "*robot_motion.rosinstall*" into a file ~/my-ws/src/.rosinstall

Fetch the code:
```sh
cd ~/my-ws/src
wstool update
```

Install the dependencies:
```sh
cd ~/my-ws
sudo rosdep init # only if never run before
rosdep install --from-paths src --ignore-src
wstool update
```

Build:
```sh
cd ~/my-ws
catkin_make
```

Further information can be found in the README.md file of the robot [motion planning], [control] and [trajectory execution] repository, respectively.



[//]: # ( ++++++++++++++++++++++++++++++++++++++++++++++ Web Links +++++++++++++++++++++++++++++++++++++++++ )

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [Gammell et al.]: <https://arxiv.org/pdf/1404.2334v3.pdf>
   [Burget et al.]: http://www2.informatik.uni-freiburg.de/~burgetf/pub/burget16iros.pdf
   [motion planning]: https://github.com/burgetf/robot_motion_planning
   [control]: https://github.com/burgetf/robot_motion_control
   [trajectory execution]: https://github.com/burgetf/robot_motion_execution
   
