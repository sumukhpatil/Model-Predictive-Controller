# Model Predictive Controller (MPC) for Assisted Lane Keeping
<img src="media/MPC.gif" width="700" height="500" />

## Introduction
In this project, a model predictive controller (MPC) is built for assisted lane keeping. This is an extension to the [PID controller](https://github.com/sumukhpatil/PID-Controller) which looked at the similar problem, but it address the drawbacks of the PID controller. The controller minimizes the cross track error, which is the value that the vehicle is off from the center of the road and the heading orientation error which helps the vehicle to be centered in the lane.
A model predictive controller (MPC) controls the process variable while satisfying a set of constraints. The model predictive controller looks at the problem as an optimization problem. It selects the trajectory with minimum cost by simulating different actuation commands. It optimizes a finite time horizon by only implementing the current timeslot and optimizes again in the next time step. MPC can anticipate future events and can take appropriate control action which make it different from a PID controller. Therefore, it is sometimes called as a receding horizon control. The GIF above shows the MPC algorithm in action.  
## Project Build Instructions
### Ubuntu
``` bash
git clone https://github.com/sumukhpatil/Model-Predictive-Controller.git
cd Model-Predictive-Controller
mkdir build && cd build
cmake ..
make
./mpc
```

## Build Dependencies
* cmake >= 3.5
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [Ipopt](https://projects.coin-or.org/Ipopt) [CppAD](https://www.coin-or.org/CppAD/)
  * Linux: run `./install-ubuntu-MPC.sh`
  * Refer `install_Ipopt_CppAD.md` for installation and troubleshooting instructions
* [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  * run `./install-ubuntu.sh` or `./install-mac.sh` depending on your platform
* Simulator
  * The simulator can be downloaded from the [Udacity GitHub Repository](https://github.com/udacity/self-driving-car-sim/releases)

## References
1. The starter code and the script to install the libraries is adopted from [Udacity GitHub Repository](https://github.com/udacity/CarND-MPC-Project)
