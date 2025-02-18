---
layout: default
---

# Cooperative Air-Ground Robot Localization


![Kalman Filter](../Images/State_Estimation.png)

The UGV’s motion is modeled kinematically here as a simple 4-wheeled steerable Dubin’s car 
![Kalman Filter](../Images/Estimation/estdyn1.png)

The fixed-wing UAV motion is modeled kinematically as a simple Dubin’s unicycle 
![Kalman Filter](../Images/Estimation/estdyn2.png)

## System Model
The nonlinear equations of motion describing the Cooperative Air-Ground Robot Localization system is defined as: 
![Kalman Filter](../Images/Estimation/estmodel1.png)

The combined system state, control inputs, and disturbance inputs are 
![Kalman Filter](../Images/Estimation/estmodel2.png)

The measurement model for the system is given by a combination of noisy ranges and azimuth angles of the UGV relative to the UAV and noisy UAV GPS measurements 
![Kalman Filter](../Images/Estimation/estmodel3.png)

## Linearization
The continuous-time nonlinear dynamics and measurement models can be linearized by first assuming that the system stays near a nominal trajectory x*(t) for some nominal control input u*
![Kalman Filter](../Images/Estimation/estlin1.png)
<br>
<img src="/Images/Estimation/estlin2.png" style="height: 300px; width:600px;"/>

Using Taylor Series expansion near x∗, the CT linearized system is approximated as:
![Kalman Filter](../Images/Estimation/estlin3.png)
![Kalman Filter](../Images/Estimation/estlin4.png)
<br>
<img src="/Images/Estimation/estlin5.png" style="height: 200px; width:400px;"/>

## Kalman Filter Block Diagram: Full “Predictor-Corrector” Cycle
![Kalman Filter](../Images/Estimation/estfilter1.png)

### KF State Estimate Errors
![Kalman Filter](../Images/Estimation/estresult1.png)

### KF State Estimates
![Kalman Filter](../Images/Estimation/estresult2.png)

## Statistical test for KF Performance
To check if KF’s state errors/measurement residuals make sense for given system + measurement + noise models

![Kalman Filter](../Images/Estimation/estperform1.png)

![Kalman Filter](../Images/Estimation/estperform2.png)
![Kalman Filter](../Images/Estimation/estperform3.png)
![Kalman Filter](../Images/Estimation/estperform4.png)
![Kalman Filter](../Images/Estimation/estperform5.png)
