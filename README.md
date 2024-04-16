# Assignment : Multiply 100 random matrices of size 2K X 2K with a constant matrix of size 2K X 2K and generate the result table, graph and CPU Usage.

## Overview :
The purpose of this project is to demonstrate the effectiveness of multi-threading in matrix multiplication tasks. Matrix multiplication is a computationally intensive operation, and parallelizing it using multiple threads can potentially improve the performance.

## Matrix Multiplication
It involves multiplying two matrices to produce a third matrix. The resulting matrix's dimensions are determined by the inner dimensions of the two input matrices. The operation is performed by taking the dot product of rows from the first matrix and columns from the second matrix.

## Methodology :
Matrix Size: Matrices of size NxN are used, where N is chosen to be sufficiently large to ensure a significant computation workload.
Constant Matrix: A constant matrix of the same size as the input matrices is generated for multiplication.
Thread Configuration: Matrix multiplication is performed using varying numbers of threads, ranging from 1 to 8.
Performance Metrics: The time taken to perform matrix multiplication with each thread configuration is measured.

## Implementation Summary
Matrix Generation: Random matrices of the specified size are generated using NumPy.
Matrix Multiplication: The matrix multiplication operation is parallelized using Python's threading module. Each thread is responsible for computing a portion of the resulting matrix.
Thread Management: Workload is divided among threads to ensure balanced computation.
Performance Measurement: The time taken for matrix multiplication with each thread configuration is recorded.
Visualization: The results are visualized using matplotlib to show the relationship between the number of threads and the time taken for matrix multiplication.

# Results :
![image](https://github.com/iosaman503/102103043_Multi_Threading/assets/90442567/d7d0a5c1-2947-4906-b4d9-ff59228dad0d)

# Critical Observations :
Initial Performance Improvement: As expected, the time taken for matrix multiplication decreases initially as the number of processes increases from 1 to 2. This improvement is due to parallelization, where multiple processes work simultaneously to compute different parts of the matrix multiplication.

Diminishing Returns: Beyond a certain point (around 2 processes in this case), the performance improvement diminishes. In fact, the time taken starts to increase as the number of processes continues to increase. This phenomenon suggests that the overhead associated with managing additional processes outweighs the benefits of parallelization for the given workload.

Performance Plateau and Overhead: From 2 processes onwards, the time taken generally increases with each additional process. This indicates that the overhead of process management, context switching, and communication between processes becomes more significant as the number of processes increases. Consequently, the performance gains from parallelization are offset by this overhead, leading to a plateau and eventual decline in performance.

System Resource Limitations: The observed behavior could also be influenced by system resource limitations. As the number of processes increases, the system's CPU cores, memory bandwidth, and other resources may become saturated, leading to reduced efficiency and performance.

# Graph :
![image](https://github.com/iosaman503/102103043_Multi_Threading/assets/90442567/cd217f90-5f33-422d-b9db-ef94ada40519)

# CPU USAGE :
![image](https://github.com/iosaman503/102103043_Multi_Threading/assets/90442567/bc1530c9-5f00-4910-b7e3-dc68070a00e8)

![image](https://github.com/iosaman503/102103043_Multi_Threading/assets/90442567/36586108-a904-4c77-bf2e-9149dae80b53)


