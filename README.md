Serial to Parallel: A Monte Carlo Operation
==================================

This tutorial covers how to build and test some serial and parallel programs to calculate π using the Monte Carlo method with MPI (distributed memory parallelism) and OpenMP (shared memory parallelism).  Although you might not be writing your own code, this exercise will give you a good idea of the benefits that parallelism can bring and how to test scalability.

####Compiling and Running
Before you start, you will need to edit the submit scripts (submit.sh and mpisubmit.sh) and the Makefile. Once done, you need to load the correct compiler environment.

First check that you have the Intel compiler suite installed:
```
module list
```
You should see something like:


To compile and submit the serial version, you need to run: ```make serial```

* For the MPI_Reduce verion: `make mpi`
* For the MPI Send/Recv verion: `make mpisr`
* For the OpenMP version: `make omp`
* For the hybrid OpenMP/MPI version: `make mpiomp`

The output should look something like:

```
Wed Sep 18 11:02:27 EDT 2013
Pi: 3.140800
Application 3587838 resources: utime ~0s, stime ~0s, Rss ~3444, inblocks ~4534, outblocks ~11970
```

The tutorial from which this code is from can be found on the OLCF website at: https://www.olcf.ornl.gov/tutorials/monte-carlo-pi/
