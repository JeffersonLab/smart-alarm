# **A Smart Alarm for Particle Accelerator Beamline Operations**
*Chris Tennant, Brian Freeman, Reza Kazimi, Daniel Moser (Jefferson Lab)* </br>
*Dan Abell, Jonathan Edelen, Joshua Einstein-Curtis (RadiaSoft LLC)*

contact: tennant@jlab.org

### Abstract
We present the initial results of a proof-of-concept “smart alarm” for the Continuous Electron Beam Accelerator Facility (CEBAF) injector beamline at Jefferson Lab. To minimize machine downtime and improve operational efficiency, an autonomous alarm system able to identify and diagnose unusual machine states is needed. Our approach leverages a trained neural network capable of alerting operators (1) when an anomalous condition exists in the beamline and (2) identifying the element setting that is the root cause. The tool is based on an inverse model that maps beamline readings (diagnostic readbacks) to settings (beamline attributes operators can modify). The model takes as input readings from the machine and computes machine settings which are compared to control setpoints. Instances where predictions differ from setpoints by a user-defined threshold are flagged as anomalous. Given data corresponding to 354 anomalous injector configurations, the model can narrow the root cause of an anomalous condition to three potential candidates with 94.6% accuracy. Furthermore, compared to the current method of identifying anomalous conditions which raises an alarm when machine parameters drift outside their normal tolerances, the data-driven model can identify 83% more anomalous conditions.

***

This repository provides companion materials to the manuscript *"A Smart Alarm for Particle Accelerator Beamline Operation"*:
- /data
    - test data: used to evaluate model performance (and create Fig. 3 from the paper)
    - simulated data: used to simulate deployed use (and create Fig. 4 from the paper)
- /model/inverse_model: saved inverse model that takes in beamline readings and predicts settings for comparision with the control system
- Jupyter notebook
