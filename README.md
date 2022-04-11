# cs284a_hw4_webpage

## Project Overview

## Part 1: Masses and springs

### Screenshots

Below are some screenshots rendered from pinned2.json file which clearly shows the structure of point masses and springs. We can cearly see the different types of springs (structural and bending constrains are totally overlapped. ) and point masses. 

![](Pic/P1/pin2_screen.png)


### Comparison Between different Constraintes

According to the definition of the three types of the constraints, we can see that the normal one (with all three constraints) have both the diagonal springs and the one which is parallel to the x or y axis. However, we can only see the diagonal springs with the shearing constraints only. And we can see the diagonal springs are moved without shearing constraints. The two left constraints (structural, bending) both depict related springs between point masses that locate nearby or 2 distance away from each other along axis. 

Type  | Picture
:---: | :---: 
With All | ![](/Pic/P1/pin2_normal.png)
Only Shearing | ![](/Pic/P1/pin2_with_only_shearing.png) 
Without Shearing | ![](/Pic/P1/pin2_without_shearing.png) 


## Part 2: Simulation via numerical integration

### Experiment
In this section, we conduct experiment on changing the parameters and show the corresponding simulation results. 

#### Change the spring constant *ks*
ks=100 | ks=5000 | ks=50000
:---: | :---: | :---:
![](/Pic/P2/ks100.png) | ![](/Pic/P2/ks5000.png) | ![](/Pic/P2/ks50000.png) 

We can see from the figure above that the balance point of the cloth collapse is getting lower as the constant *ks* increases. This is caused by the fact that the spring force to support the cloth will increase when the constant *ks* increases. Therefore, when the constant decreases, the cloth will collapse and fall down to a lower balance point. 

#### Change *density*
density=1 | density=1500
:---: | :---:
![](/Pic/P2/density1.png) | ![](/Pic/P2/density1500.png) 

Similar to changing the spring constant, we can see the balance point get lower as *density* increases. The mass of a point mass increase as the density increases. Therefore, the external force *F=m*a* will increase as *m* (mass) increases, which produce the similar results as *ks* increases (the internal force by the spring increases).

#### Change *damping*
Changing damping does not affect the force. Therefore, the balance point of the cloth (final real estate status) will not change. We can see from our ***simulate*** function that the parameter *damping* only changes the position update process. To be more specific, *damping* affects the weight of the difference between a pointmass's current position and last poisiton. The *damping* simluate the loss of energy. Therefore, larger *damping* will result in slower simulation and more stable final state. And smaller *damping* results in faster swing but less stable final state (need more time to converge to a immobile state.) 

The extreme case are interesting. We will find the cloth keep swinging back and forth when we set *damping=0*, which means there are no energy loss due to factors such as friction. This is straightforward because the sum of Kinetic and Potential Energy will remain a constant in the whole process. 

#### Screenshot: *pinned4.json*
Below are the final state of the rendered *pinned4.json* file. (default parameter)

![](/Pic/P2/pin4.png)


## Part 3: Handling collisions with other objects



## Part 4: Handling self-collisions

## Part 5: Shaders

