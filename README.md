# Kalman-Filtering-for-GPS-Trajectory-Data
Designed a Kalman Filter, Extended Kalman Filter, and Unscented Kalman for the Microsoft GeoLife dataset to estimate vehicle altitude, velocity, and acceleration.

A practical, from-scratch exploration of Kalman filtering on real GPS trajectories. This repo implements and compares Kalman Filter (KF), Extended Kalman Filter (EKF), and Unscented Kalman Filter (UKF) for altitude-denoising and state estimation, including tuning and out-of-sample testing on a second trajectory. Variable timesteps and noisy altitude, just like real life.

Project goals and scope
Goal: Filter noisy GPS altitude and estimate hidden dynamics (velocity, acceleration) with interpretable uncertainty.

Filters: Classical KF (linear), EKF (local linearization), UKF (sigma-point transform), plus URTS smoothing.

Use cases:

Pure filtering: all states measured or computable.

State estimation: some states unmeasured (filter infers them).

Focus variable: Altitude (noisiest channel in Geolife), with velocity and acceleration derived via finite differences.

Evaluation: Innovation RMS and average variance by state, runtime, qualitative smoothing on train and test trajectories.


# Project Structure
- `src/` – Core Python scripts for all Kalman filters
- `data/` – Visuals of Selected Kalman Filters
- `docs/` – Detailed project report
