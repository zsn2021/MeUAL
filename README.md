# MeUAL: Model-enhanced Uncertainty-aware Augmented Lagrangian for Safe Decision-Making and Control in Autonomous Highway Overtaking

## Table of Contents

- [1. Decision-Making and Control Framework Based on MeUAL](#1-decision-making-and-control-framework-based-on-meual)  
- [2. Driving Scenario Setup](#2-driving-scenario-setup)  
- [3. Analysis of the Overtaking Behavior of MeUAL-PSM](#3-analysis-of-the-overtaking-behavior-of-meual-psm)  

---

## 1. Decision-Making and Control Framework Based on MeUAL
<img width="5294" height="3275" alt="fig2" src="https://github.com/user-attachments/assets/0669b393-ef4b-47f1-99f5-e1fce5212e30" />

Decision-making and control framework based on MeUAL.

---

## 2. Driving Scenario Setup

### 2.1 Scenario Configuration

| **Component**                   | **Description**                                                                                                                                  |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **Simulator**                   | Highway-env simulator for traffic scenario construction                                                                                         |
| **Ego Vehicle Initial Speed ($v_0$)** | 25 m/s                                                                                                                                       |
| **Surrounding Vehicles Initial Speed ($v_i$)** | Randomly generated between [21, 24] m/s                                                                                                   |
| **Surrounding Vehicles Control Models** | IDM for longitudinal control and MOBIL for lateral lane-changing                                                                            |
| **Vehicle Length**              | 5 m                                                                                                                                             |
| **Vehicle Width**               | 2 m                                                                                                                                             |
| **Lane Configuration**          | Four-lane highway with lane width of 4 m                                                                                                        |
| **Politeness Coefficient (MOBIL)** | Set to 0, meaning surrounding vehicles are not considered when changing lanes                                                                 |
| **Acceleration Coefficient (IDM)** | Randomly selected between [3.5, 4.5] m/s²                                                                                                     |
| **Lane Selection**              | Randomly selected from four available lanes (L1, L2, L3, L4)                                                                                    |
| **Position Noise**              | Longitudinal offset $\Delta x_i$ adjusted by a uniform random number between 0.9 and 1.1 to simulate noise                                       |
| **Number of Surrounding Vehicles** | 20                                                                                                                                             |
| **Simulation Platform**         | Scenario reconstructed in CARLA for a more realistic environment                                                                                |
| **State Information**           | Ego vehicle and surrounding vehicles’ states (position, velocity, heading) assumed to be accurately obtained within the perception range         |
| **Gaussian Noise**              | Added to state information to simulate perception-level noise                                                                                   |

### 2.2 Schematic Diagram of Highway Simulation Scenario

- **Highway-env**  
<img width="900" alt="fig4" src="https://github.com/user-attachments/assets/11ff84c9-9218-417b-98c6-4560aece3a49" />

Schematic diagram of a four-lane highway. The red car represents the ego vehicle, while the white cars represent the surrounding vehicles.  

- **CARLA**  
<img width="900" alt="CARLA_env" src="https://github.com/user-attachments/assets/fe68d27e-7bdc-498e-9275-70c9b817c60b" />

The highway simulation scenario reconstructed in CARLA.

---

## 3. Analysis of the Overtaking Behavior of MeUAL-PSM

#### 3.1 IDM + MOBIL

https://github.com/user-attachments/assets/0856957f-f72f-4060-b606-232452ffdbda

Multiple Perspectives of Highway Simulation Scenarios in CARLA.

![Dynamic Driving Risk Field (IDM + MOBIL)](https://github.com/user-attachments/assets/62295dfb-c782-4c4e-8e9b-4970a806963c)

Dynamic Driving Risk Field.

---

#### 3.2 MeUAL

https://github.com/user-attachments/assets/6a521b76-0349-4524-a428-b7c947bd90ad

Multiple Perspectives of Highway Simulation Scenarios in CARLA.

![Dynamic Driving Risk Field (MeUAL)](https://github.com/user-attachments/assets/615da2bc-5fc9-4e1c-8ced-f5fa4609436b)

Dynamic Driving Risk Field.

---

#### 3.3 MeUAL-PSM


https://github.com/user-attachments/assets/2186ceff-4bef-41ec-a89f-00bc62c55ef3

Multiple Perspectives of Highway Simulation Scenarios in CARLA.

![Dynamic Driving Risk Field (MeUAL-PSM)](https://github.com/user-attachments/assets/59bb246e-c50e-41f0-8c7c-d8c46366f4d7)

Dynamic Driving Risk Field.
