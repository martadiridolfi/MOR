# Parametric Nonlinear Elliptic Problem: a comparison of POD, PINNs and POD-NN
## Overview
In the present study, the solution of a nonlinear elliptic problem is computed with the purpose of highlighting and analyzing the main differences between three methods of Model Order Reduction theory: POD, PINN and POD-NN.
Firstly, the code implemented was tested on a benchmark problem and then it was adjusted in order to solve the project task. The numerical results are compared with the theoretical ones. 

## How to use this repository

The Jupyter notebook is organized into three main sections:

- Section 1: Galerkin-POD approach
- Section 2: PINN method
- Section 3: POD-NN approach (Proper Orthogonal Decomposition integrated with NNs)

### Section Details

- Method Application: This section includes the code required to implement the related method.

- Benchmark Testing: In this section, the methods are first tested on the benchmark problem for which we have known solution.

- Project Task Implementation: After benchmarking, the methods are applied to the specific project task.

### Analysis

For each method, we have conducted:

- Error Analysis
    Detailed examination of the $H^1$, $L^2$ errors associated with the method.
- Speed-Up Analysis
    Comparative analysis of the computational speed relative to the classically used Galerkin POD method.

### Usage

- Loading Models:
    The repository includes pre-trained PINNs and FFNNs models that can be easily loaded for inference.

- Running the Notebook:
    Follow the steps in each section of the notebook to reproduce the results and apply the methods to your own tasks.

## Conclusion
The three techniques evaluated in this report—Proper Orthogonal Decomposition (POD), Physics-
Informed Neural Networks (PINNs), and POD-Neural Network (POD-NN)—represent three different
approaches to model order reduction, aiming to decrease time and computational costs while main-
taining a reasonable accuracy in the solution of a parametric nonlinear elliptic problem.
By comparing the performance of the three methods we can highlight that the POD algorithm is the
most accurate in terms of average relative errors in L2 and H1
0 norms w.r.t. the high fidelity solution, as
reported in Table 7. However, due to the non-linearities in our problem, it fails to significantly reduce
the computational time of FOM. In contrast, the PINN approach demonstrates enhanced inference
speed but lower precision in solution prediction, with errors three orders of magnitude greater than
those of the POD. Ultimately, the **POD-NN** method emerges as the most promising, achieving a
balance between inference speed and precision. It provides results nearly as precise as those of the
POD but with significantly lower inference time. In conclusion, the POD method is preferable in case
of linear variational problems; the PINN is the worst ROM and the POD-NN the best one for the
approximation of a reduced solution of the parametric nonlinear elliptic problem solved in the present work.




