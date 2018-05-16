1.) Describe the effect each of the P, I, D components had in your implementation.

The P, or "proportional", component had the most directly observable effect on the car's behavior. It causes the car to steer proportional (and opposite) to the car's distance from the lane center (which is the CTE) - if the car is far to the right it steers hard to the left, if it's slightly to the left it steers slightly to the right.

The D, or "differential", component counteracts the P component's tendency to ring and overshoot the center line. A properly tuned D parameter will cause the car to approach the center line smoothly without ringing.

The I, or "integral", component counteracts a bias in the CTE which prevents the P-D controller from reaching the center line. This bias can take several forms, such as a steering drift (as in the Control unit lessons).

2.)Describe how the final hyperparameters were chosen.

All the 3 hyperparameters PID (proportional/integral/differential) were tuned manually. Initially  all the parameters were set to 0 then after tuning the parameter maually i obsereved the result and finally i found that my controller is giving good and non-jerky behavior of car with the following values of hyperparameters p=0.2 ,I=0.004 ,D=3.0 . Throttle value can be adjusted according to the processor of the system. For smooth movement of car i have set the throttle value as 0.05 according to processor.