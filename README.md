# MPI-API

parallelize vector operations  using MPI API

You are given a vector v 2 RN. Initialize your vector v with random numbers (can be either integers or 
oating points). You will experiment with three different sizes of vector, i.e. N = f107; 1012; 1015g.
You have to parallelize vector operations mentioned below using MPI API. For each operation you will
have to run experiment with varying number of workers, i.e. if your system has P workers than run
experiments with workers = f1; 2; : : : Pg for each size of vector given above. You have to time your
code for each operation and present it in a table. 

MPI point-to-point communication i.e. Send and Recv.
Add two vectors and store results in a third vector.
Find an average of numbers in a vector.
