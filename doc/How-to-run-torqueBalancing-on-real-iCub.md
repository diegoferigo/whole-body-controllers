
## HOW TO RUN BALANCING WITH TORQUE CONTROL ON ICUB

The procedure to run the torque balancing module is still quite elaborate. Users willing to use the module should follow this list.

- Set the environmental variable `YARP_ROBOT_NAME` in the `.bashrc` according to the robot one wants to use (e.g. icubGazeboSim for simulations, or iCubGenova04, etc. for experiments). Please **note** that for the time being, the same environmental variable must be set also in the Matlab environment, by properly choosing the `YARP_ROBOT_NAME` in the controllers' [initialization script](https://github.com/robotology/whole-body-controllers/blob/master/torque-controllers/momentum-based-yoga/initTorqueBalancingYoga.m).
 
#### Before putting the robot feet on the ground:

- Bring the robot in a suitable home position (e.g. `$ yarpmotorgui --from homePoseBalancing.ini` and then select a custom position by clicking on `Global Joints Commands/Custom postions`.

- Type on a terminal `yarp rpc /wholeBodyDynamics/rpc` and execute the command `calib all 300`. It will remove offsets from FT sensors measurements.

- Then, put the robot on the ground.

#### After putting the robot on the ground:

- Open the simulink model and run the module.

#### Citing this contribution
In case you want to cite the content of this module please refer to [iCub whole-body control through force regulation on rigid non-coplanar contacts](http://journal.frontiersin.org/article/10.3389/frobt.2015.00006/abstract) and use the following bibtex entry:

```
@INPROCEEDINGS{Nava_etal2016, 
author={G. Nava and F. Romano and F. Nori and D. Pucci}, 
booktitle={2016 IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)}, 
title={Stability analysis and design of momentum-based controllers for humanoid robots}, 
year={2016}, 
pages={680-687}, 
keywords={Lyapunov methods;asymptotic stability;closed loop systems;control system synthesis;humanoid robots;legged locomotion;linearisation techniques;momentum;robust control;Lyapunov analysis;balancing controller design;closed loop system asymptotic stability;iCub humanoid robot;linearized system joint space;momentum-based controller design;robust controllers;stability analysis;unstable zero dynamics;walking controller design;Acceleration;Asymptotic stability;Humanoid robots;Legged locomotion;Robot kinematics;Stability analysis}, 
doi={10.1109/IROS.2016.7759126}, 
month={Oct},}
```

```
 @article{Nori_etal2015,
 author="Nori, F. and Traversaro, S. and Eljaik, J. and Romano, F. and Del Prete, A. and Pucci, D.",
 title="iCub whole-body control through force regulation on rigid non-coplanar contacts",
 year="2015",
 journal="Frontiers in {R}obotics and {A}{I}",
 volume="1"
 }
```
