# Robust_Distributed_State_Estimation_Dataset
Dataset for the paper entitled "Opt-ADMM-Net: A Novel Learn-to-Optimize Architecture for Robust Distributed State Estimation".

### Simulation settings:

The IEEE-30 bus testing system is utilized and divided into three distinct areas in our cases studies. True system states are obtained by running probabilistic power flow calculations using the given parameters in Matpower cases files. Measurements dataset are simulated by adding zero-mean Gaussian noise, with a standard deviation of $\sigma = 0.001$ p.u., to the ground-truth values. Outliers are simulated by amplifying the $\sigma$ by 50 times under a certain penetration rate 10\%. Then, 500 samples are partitioned into a training set and a testing set at an 8:2 ratio. All simulations are implemented by Matlab 2024a and Python 3.10 with PyTorch and CVXPY packages on a personal computer and optimization problems are solved by Gurobi. The hardware environment is Intel i7-14700F CPU and NVIDIA GeForce RTX 4060Ti GPU.

The hyperparameters configured for the Opt-ADMM-Net are set as follows. Learning rate $\alpha= 1e-3$, weight decay factor $\zeta=1e-4$, batch size $B=32$, training epoch $E=50$ and iteration times $T=30$. The exponential decay rates of Adam, denoted by $\beta_1$ and $\beta_2$, are set as 0.9 and 0.999 by default. $\epsilon$ is set as 1e-5.
