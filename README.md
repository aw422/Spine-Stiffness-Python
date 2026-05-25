# Lumbar Spine Stiffness Analysis Pipeline

This repository contains a data processing pipeline developed to analyze human spinal kinematics. The code translates a legacy MATLAB data-processing workspace into Python to maximize data flexibility and processing efficiency.

## Project Overview
The primary objective of this project was to quantify an individual's *in vivo*, through-range, axial-rotation lumbar spine stiffness. 

### Experimental Methodology
1. **Physical Constraints:** The subject's torso was securely fixed above the T12 vertebrae while standing on a custom rotating platform. The platform was turned at a fixed rate using a mechanical winch system.
2. **Sensor Deployment:** Inertial Measurement Units (IMUs) were positioned at the T12 and S1 spinal levels to capture segmental kinematics. An additional IMU was mounted directly to the winch handle to be used for data catprue start and end time signatures. A force transducer was attached to the cable connecting the winch to the rotating platform capturing the force used to rotate the platform.
3. **Data Acquisition:** The system captured the continuous force required to actuate the platform alongside the precise change in Yaw from the T12 and S1 IMUs. 

Using these multi-sensor streams, the pipeline filters raw signal noise, isolates the relative range of movement, and calculates the discrete through-range stiffness of the lumbar spine during axial rotation.

## Technical Stack & Libraries
This pipeline is written in Python (Jupyter Notebook format) and leverages standard data-science libraries:
* **NumPy:** For matrix operations, coordinate transformations, and mathematical modeling.
* **Pandas:** For importing, cleaning, and structuring messy, time-synchronized CSV/Excel sensor outputs.
* **Matplotlib** For generating kinematic signal and load-displacement plots.
* **SciPy:** Used for signal conditioning, data filtering (e.g., Butterworth low-pass filtering), and numerical derivatives.

## Project Origin
This pipeline represents an independent technical translation and optimization of custom MATLAB algorithms originally developed for spinal biomechanics research.
