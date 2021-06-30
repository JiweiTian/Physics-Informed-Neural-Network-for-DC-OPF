# Physics-Informed-Neural-Network-for-DC-OPF
This repository contains the code for Physics-Informed Neural Network for DC Optimal Power Flow applications and the worst case guarantees

Author: Rahul Nellikkath
E-mail: rnelli@elektro.dtu.dk

This code is distributed WITHOUT ANY WARRANTY, without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

This code requires the following:

- conda(python) and tensor flow installations with environment activated 
- Matlab (R2018b) or above
- YALMIP (https://yalmip.github.io/download/)
- Gurobi (Gurobi V9.1.2, https://www.gurobi.com/)
- MATPOWER (matpower7.1, https://matpower.org/)

The data for the test cases are reproduced from the IEEE PES Power Grid Library - Optimal Power Flow - v19.05 (https://github.com/power-grid-lib/pglib-opf)

To run the code to re-create the simulation results please follow the steps below:
	0.Run "A1_Create_Test_Cases" and "A2_Create_Data_Sets" to generate the data sets
	1.Run PINN_DC_OPF_Main.py in python: 
		1.1 It contains the python code used for the PINN algorithms
		1.2 Teset cases can be 39 bus system, 118 bus system or 162. They can be changed by changing the "n_buses"
		1.3 All the fuctions used by the algorith is given in Folder PINNs
		1.4 After the training the weigts and biases will be stored in the respective folder in:"MILP_For_Worst_Case_Guarantees\Trained_Neural_Networks"
	2. Run "Evaluate_Average_And_Worst_Performance_Data.m" to get results from the data
	3. The Run "E2" - "E4" to get the worst case performance.  
