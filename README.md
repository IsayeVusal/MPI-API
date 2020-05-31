# MPI-API

Parallelize vector operations  using MPI API

You are given a vector v 2 RN. Initialize your vector v with random numbers (can be either integers or 
oating points). You will experiment with three different sizes of vector, i.e. N = f107; 1012; 1015g.
You have to parallelize vector operations mentioned below using MPI API. For each operation you will
have to run experiment with varying number of workers, i.e. if your system has P workers than run
experiments with workers = f1; 2; : : : Pg for each size of vector given above. You have to time your
code for each operation and present it in a table. 

Nonblocking Point-to-Point Communication
The point-to-point communication calls MPI_Send and MPI_Recv, do not return from the respective function call until the send and receive operations have completed. While this ensures that the send and receive buffers used in the MPI_Send and MPI_Recv arguments are safe to use or reuse after the function call, it also means that unless there is a simultaneously matching send for each receive, the code will deadlock, resulting in the code hanging. One way to avoid this is by using nonblocking point-to-point communication.

Nonblocking point-to-point communication returns immediately from the function call before confirming that the send or the receive has completed. These nonblocking calls are MPI_Isend and MPI_Irecv. They are used coupled with MPI_Wait, which will wait until the operation is completed. When querying whether a nonblocking point-to-point communication has completed, MPI_Test is often paired with MPI_Isend and MPI_Irecv. Nonblocking point-to-point calls can simplify code development to avoid such deadlocks more easily and also potentially enable the overlap of useful computation while checking to see if the communication has completed.

MPI point-to-point communication i.e. Send and Recv.
Add two vectors and store results in a third vector.
Find an average of numbers in a vector.
