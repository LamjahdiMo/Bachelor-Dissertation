# Dynamic Control of Rolling Force in Mechanical Deep Rolling

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15809105.svg)](https://doi.org/10.5281/zenodo.15809105)
## About the Thesis

This bachelor’s thesis addresses the development, simulation, and implementation of a control system for the dynamic regulation of rolling force during mechanical burnishing. The focus is on managing transfer stagnation and disturbances in the rolling process using modern control engineering approaches such as PID controllers, Smith predictors, and innovative estimation methods.

## Hyperlinks
- [Bachelorthesis](Bachelor_Thesis)
- [Solving Linear Systems in O(1): The 2X, Matrix Inversion, and Gitter Methods](Bachelor_Thesis/O(1)-Methods) [![DOI](https://zenodo.org/badge/DOI/10.17605/OSF.IO/52MWX.svg)](https://doi.org/10.17605/OSF.IO/52MWX)
- [6X-Method for solving 4x4 Linear Equations in O(1)](Bachelor_Thesis/O(1)-Methods/6X.pdf)
- [Noticed Copyright Infringement](Copyright_Infrimgment)

## Objective of the Thesis

The aim is to develop an intelligent control concept that:

- Compensates for transfer stagnation caused by communication delays  
- Filters out external disturbances  
- Regulates the burnishing force in a position-dependent manner and in real time  
- Can be implemented on an industrial PC (IPC) using TwinCAT

## Methodology

The work is structured into several phases:

1. **Theoretical Foundations & Literature Review**
   - Control engineering, LTI systems, Laplace transformation, PID, I, D controllers  
   - Bode diagram, stability criteria (Nyquist, Hurwitz)

2. **Analysis of the Rolling Process**
   - Characterization of burnishing behavior  
   - Problematic influences such as dead time and disturbances

3. **Control Approaches**
   - PID controllers with and without modifications  
   - Smith predictor to compensate for dead time  
   - Two custom-developed estimators (M.A. and M.E. estimators)

4. **Simulation & Verification**
   - MATLAB/Simulink, SolidWorks, Ansys  
   - TwinCAT programming, Beckhoff dashboard  
   - Testing under realistic and extreme conditions

## Results

- The combination of real-time moving average estimation, Smith feedforward, and optimized PID parameters provides the most stable and efficient control  
- The developed estimators significantly improved responsiveness  
- The resulting solution is robust against disturbances and suitable for industrial applications

## Technologies & Tools

- **Simulink / MATLAB**  
- **Beckhoff TwinCAT / Windows Control**  
- **Python** (for analysis & data processing)  
- **SolidWorks, Ansys**  
- **OPC-UA** for communication between control system and sensors

## Supervisors & Examiners

- **Institute:** Institute of Production Engineering and Machine Tools (IFW)  
- **First Examiner:** Prof. Dr.-Ing. Bernd Ponick  
- **Second Examiner:** Prof. Dr.-Ing. Berend Denkena  
- **Supervisor:** MSc. Jan, Berlin

## Submission

- **Date:** September 2024  
- **Location:** Garbsen / University of Hanover

## Note

This thesis was completed independently. All assistance is cited in the bibliography. The source code and executable implementations are not included in this repository and can be obtained from the author upon request.

---


