# Embedded Systems and Parallel Programming in C

Two individual university assignments implemented in C for an embedded and real-time systems course. The repository combines a parallel nearest-neighbour experiment with a concurrent producer-consumer simulation.

## Projects

### Parallel k-NN with OpenMP and OpenBLAS

`Ergasia0.c` implements a nearest-neighbour search over 20,000 points in a 10-dimensional space. The implementation uses OpenBLAS for distance calculations, OpenMP tasks for parallel work distribution, and Quickselect to avoid fully sorting every distance vector.

- Source: `Ergasia0.c`
- Build: `make`
- Run: `./Ergasia0`
- Report: [parallel k-NN with OpenMP and OpenBLAS](reports/parallel_knn_openmp_openblas_report_gr.pdf) 

### Producer-Consumer with POSIX Threads

`pc.c` models a dynamic FIFO task queue shared by producer and consumer threads. Producers add work packages and consumers execute the stored mathematical operations, with synchronization handled through POSIX threads.

- Source: `pc.c`
- Build: `gcc -O3 pc.c -o producer_consumer -pthread -lm`
- Run: `./producer_consumer <producers> <consumers>`
- Report: [producer-consumer with pthreads](reports/producer_consumer_pthreads_report_gr.pdf) 

## Requirements

- GCC or a compatible C compiler
- OpenMP and OpenBLAS for the parallel k-NN program
- POSIX threads for the producer-consumer program

## Repository structure

```text
.
├── Ergasia0.c # parallel k-NN implementation
├── pc.c # producer-consumer implementation
├── Makefile # build target for the k-NN program
└── reports/ # accompanying coursework reports in Greek
```
