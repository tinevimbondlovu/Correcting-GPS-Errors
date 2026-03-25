# Correcting-GPS-Errors
Exploring Techniques to improve GPS accuracy


The goal of this project is to estimate receiver position in ECEF coordinates using raw GNSS logs and broadcast ephemeris data. User position is first solved using iterative least squares, and then the project attempts to improve positioning accuracy by addressing key GNSS error sources: <br />
- Receiver clock Bias <br/>
- Satellite clock error <br/>
- Earth rotation (Sagnac Effect)
- Satellite geometry
- Ionspheric range error (work in progress)

Another way to estimate receiver position is to use an Extended Kalman Filter (EKF). The EKF in this project is used to refine GPS position estimates over time by fusing sequential pseudorange measurements with a motion model. It improves upon the standalone least squares solution by estimating not only position, but also velocity and receiver clock bias/drift, while accounting for measurement noise and system dynamics.
