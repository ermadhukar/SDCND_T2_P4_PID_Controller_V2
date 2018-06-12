# Self-Driving Car PID Controller

In this Project a PID controller is being coded to tune the steering angle of the car, so that it will remain on the track while running autonomously. The code has been writeen in C++ and being simulated in the class Simulator.


## Dependencies

* cmake >= 3.5
* make >= 4.1
* gcc/g++ >= 5.4
* uWebSockets
* Simulator

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`. 

## P-I-D Coefficients

> Proportional coefficient, Kp: It determines the speed of response for the loop. The higher the  gain, the faster the loop responds. However, higher gains lead to overshoot and oscillations in the response. 

> Integral Coefficient, Ki: The integral component sums the error term over time. The result is that even a small error term will cause the integral component to increase slowly. The integral response will continually increase over time unless the error is zero, so the effect is to drive the Steady-State error to zero

> Differential Coefficient, Kd: It reduces the overshoot and oscillations. It is reponsbile for dampening of the oscillation by being responsive to the rate of change of error. It will delay the desired state but will also reduce the overshoot and oscillations. 

## Coefficients Characteristics
> If Kp is set high, it will cause Car to oscillate too much. There will be big  overshoot, which may cause vehicle to go oftrack. 
> If Ki is set high, the car may tends to have faster oscillations.
> If Kd is set high, car will bobble across the target. 

## Parameter Selection
PID coefficients has been identified by try and error. It has been initialized with all parameters as zero. After that all other parameters, Proportional, Differential and Integrator has been tuned sequentially. For these parameters vehicle behavior has been monitored. 

# Output
![](https://github.com/ermadhukar/SDCND_T2_P4_PID_Controller_V2/blob/master/Img/T2P4_1.png)

![](https://github.com/ermadhukar/SDCND_T2_P4_PID_Controller_V2/blob/master/Img/T2P4_2.png)

![](https://github.com/ermadhukar/SDCND_T2_P4_PID_Controller_V2/blob/master/Img/T2P4_3.png)
