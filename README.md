# Vehicle Localization on a Racetrack – LNSM Course Project

## Overview
This repository contains the course project for **Localization, Navigation and Smart Mobility (LNSM)** at Politecnico di Milano.  
The project focuses on **localizing a moving vehicle on a racetrack** using Ultra-Wideband (UWB) signals from the Ubisense Dimension 4 system, with measurements of **Time Difference of Arrival (TDoA)** and **Angle of Arrival (AoA)**.  
Multiple localization algorithms are implemented in MATLAB and compared against high-accuracy **GPS RTK** ground truth.

---

## Methodology
- **Data Acquisition**:  
  - 10 UWB Access Points (APs) deployed around the track.  
  - 4 UWB tags mounted on the vehicle.  
  - GPS RTK modules providing reference ground truth.  
  - Data sampling rate: 10 Hz.

- **Localization Methods**:  
  1. **TDoA-only**: Least-squares position estimation from range-difference measurements.  
  2. **AoA-only**: EKF-based tracking using azimuth/elevation data.  
  3. **Hybrid TDoA + AoA**: Joint least-squares estimation with outlier removal (Hampel filter) and Kalman smoothing.

- **Tracking & Filtering**:  
  - **Extended Kalman Filter (EKF)** for AoA-only method.  
  - **Constant velocity motion model**.  
  - **Noise tuning via NIS-based adaptation**.

- **Performance Evaluation**:  
  - RMSE, MAE, 95% Quantile error.  
  - Availability & reliability analysis.  
  - Comparison against GPS RTK ground truth.

