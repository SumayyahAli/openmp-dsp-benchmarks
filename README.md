# Digital Signal Processing & Image Processing | (Serial C vs OpenMP) Benchmarks

This project evaluates the performance of common Digital Signal Processing and Image Processing algorithms implemented in C and parallelized using OpenMP.
No advanced OpenMP optimization was applied; the focus is to see how adding minimal OpenMP directives to serial C code affects runtime behavior across different data sizes.
The results highlight the trade-off between compute intensity and parallel overhead on multicore CPUs.


| Algorithm                 | Domain            | Description                                                      |
| ------------------------- | ----------------- | ---------------------------------------------------------------- |
| **Sobel Filter**          | Image Processing  | Edge detection using horizontal & vertical kernels      |
| **Moving Average Filter** | Signal Processing | Simple smoothing filter using a sliding window                   |
| **FIR Low-Pass Filter**   | Signal Processing | Finite Impulse Response convolution filter for low-pass response |

## Environment and Methodology

- **Hardware:** Intel® i9 CPU (14 cores, 20 processors )  
- **Compiler:** GCC with `-O3 -fopenmp`
- **Timing:** `omp_get_wtime()` averaged over 3 runs  
- **Threads:** Default OpenMP configuration (`omp_get_max_threads()` = all logical processors).
- **MATLAB usage:** Generating signals, designing FIR coefficients, and plotting results


## Sobel Filter

<img width="800" height="1600" alt="image" src="https://github.com/user-attachments/assets/c9817bd9-da0d-46e0-a92b-203ad885a6fa" />

## FIR (Low-Pass Filter)

<img width="800" height="1600" alt="image" src="https://github.com/user-attachments/assets/c25f85d2-47cf-4e8c-8f6f-d6ff20d7ddf9" />


## **Moving Average Filter**

<img width="800" height="1600" alt="image" src="https://github.com/user-attachments/assets/98f2f889-c268-4c9e-ad4e-285d334b19d5" />




