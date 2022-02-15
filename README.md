# Reservoir Computing for superimposed sine wave modeling
This is a work-in-progess project to model the periodic behavior of superimposed sine waves. For this purpose an Echo State Network (ESN) is implemented in Python using NumPy, consisting of an Input Layer, the recurrent layer (the Reservoir) and the Output Layer. The Input Layer projects the signal to the Reservoir for a certain amount of timesteps, while replacing the output with the true target (Teacher Forcing). Then, the error is measured for another amount of timesteps (Training) and afterwards the Reservoir runs in a Closed Loop using a set of feedback weights. All weight matrices (Win, Wr, Wout, Wfb) are initialized based on known principles: they are reasonable small (e.g. 1e^-10), they have a sparse nature (e.g. only 20% of the entries are non-zero), and the weight matrix of the Reservoir Wr fulfils the Echo State Property to maintain robust reservoir dynamics. This will asymptotically wash out initial signals and is given if the largest eigenvalue of Wr is smaller than 1. Optimal ... can be yielded by the pseudoinverse algebra:

One solution to find sufficient parameter values is by using Evolutionary Algorithms. In this case, Differential Evolution (DE) is applied with parameters Population Size, Maximum Number of Generations, Mutation Rate and Crossing Over probability.

![Scheme2](https://user-images.githubusercontent.com/56418155/154161445-821c6cc4-4b8d-49a9-9ff9-a6cba1c56f9f.png)


![Scheme](https://user-images.githubusercontent.com/56418155/154161251-8e432ef8-970a-4b1b-9e40-34779225dd02.png)
