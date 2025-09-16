# MeUAL: Model-enhanced Uncertainty-aware Augmented Lagrangian for Safe Decision-Making and Control in Autonomous Highway Overtaking

## 目录

- [1. Driving Scenario Setup](#1-driving-scenario-setup)
- [3. Experimental Results and Discussion](#3-experimental-results-and-discussion)
  - [3.1 Analysis of the Overtaking Behavior of MeUAL-PSM](#31-analysis-of-the-overtaking-behavior-of-meual-psm)


## 1. Decision-Making and Control Framework Based on MeUAL
<img width="5294" height="3275" alt="fig2" src="https://github.com/user-attachments/assets/0669b393-ef4b-47f1-99f5-e1fce5212e30" />


## 1. Driving Scenario Setup

### Environment Configuration

| **Component**              | **Description**                                                                                                                                      |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Simulator**               | Highway-env simulator for traffic scenario construction                                                                                             |
| **Ego Vehicle Initial Speed ($v_0$)** | 25 m/s                                                                                                                                           |
| **Surrounding Vehicles Initial Speed ($v_i$)** | Randomly generated between [21, 24] m/s                                                                                                       |
| **Surrounding Vehicles Control Models** | IDM for longitudinal control and MOBIL for lateral lane-changing                                                                                |
| **Vehicle Length**          | 5 m                                                                                                                                                 |
| **Vehicle Width**           | 2 m                                                                                                                                                 |
| **Lane Configuration**      | Four-lane highway with lane width of 4 m                                                                                                            |
| **Vehicle Politeness Coefficient (MOBIL)** | Set to 0 to disregard surrounding vehicles when changing lanes                                                                                  |
| **Acceleration Coefficient (IDM)** | Randomly selected between [3.5, 4.5] m/s²                                                                                                       |
| **Lane Selection**          | Randomly selected from four available lanes (L1, L2, L3, L4)                                                                                      |
| **Position Noise**          | Longitudinal position offset $\Delta x_i$ is adjusted with a random number uniformly distributed between 0.9 and 1.1 to simulate noise             |
| **Number of Surrounding Vehicles** | 20                                                                                                                                               |
| **Simulation Platform**     | Reconstructed in CARLA for more realistic environment                                                                                              |
| **State Information**       | The ego vehicle and surrounding vehicles' state information (position, velocity, heading) are accurately obtained within the perception range      |
| **Gaussian Noise**          | Added to the state information to simulate perception-level noise                                                                                  |

### Visual Representation

- **Highway Scenario**:
<img width="2275" height="881" alt="fig4" src="https://github.com/user-attachments/assets/11ff84c9-9218-417b-98c6-4560aece3a49" />

- **CARLA Simulation**: 

<img width="2188" height="813" alt="CARLA_env" src="https://github.com/user-attachments/assets/fe68d27e-7bdc-498e-9275-70c9b817c60b" />


## 3. Analysis of the Overtaking Behavior of MeUAL-PSM

- **IDM+MOBIL**:
https://github.com/user-attachments/assets/163f5421-8a28-46f8-985c-39d7e61e1497
Multiple Perspectives of Highway Simulation Scenarios in CARLA
![IDM+MOBIL](https://github.com/user-attachments/assets/25d893bd-aed3-494c-b94e-a2560e4cfae5)
行驶风险场动态图

- **MOBIL**:
https://github.com/user-attachments/assets/0a8925ec-101f-4be1-864e-18d21e74755f
Multiple Perspectives of Highway Simulation Scenarios in CARLA
![MeUAL](https://github.com/user-attachments/assets/d32356c5-2442-44ae-aca3-2331a63fcf74)
行驶风险场动态图


- **MOBIL-PSM**:
https://github.com/user-attachments/assets/fa3a1a43-4275-4e54-a79f-69e7c439ee53
Multiple Perspectives of Highway Simulation Scenarios in CARLA

![MeUAL-PSM](https://github.com/user-attachments/assets/f1d4b54c-821e-4d9a-8b03-424a03b49b40)
行驶风险场动态图





