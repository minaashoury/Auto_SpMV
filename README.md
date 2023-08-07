# Auto_SpMV

This repository contains codes and dataset have been used for optimizing the performance and energy efficiency of sparse matrix-vector (SpMV) multiplication kernels using various storage formats in CUDA. 
"Codes.rar" includes codes for converting matrices in COO format to other formats and also the SpMV kernels processing that specific matrix representation. These kernels aim to tune Compiler parameters such as maximum number register per thread (maxrregcount),memory hierarchy configuration, and thread block size for input sparse matrices, enabling users to auto-tune these parameters for the best SpMV kernel as predicted by machine learning methods. 
"dataset.csv" includes all the GPU results that are used by different classifiers to optimize performance and energy efficiency of SpMV kernels. 

Compiling and Executing Code

These SpMV kernels are developed in Visual Studio 2017.


1. Start Visual studio 2017 (any edition)
2. Create a Cuda project
3. Add files of Codes.rar to the project
4. Link "nvml.lib" in visual studio project properties
5. build the project
6. firstly, convert a Sparse Matrix in .mm format to the arbitrary format using convertor functions files in codes.rar
7. Secondly, run a SpMV Kernel (.cu) (A thread will capture the instant power consumption while another thread is lunching the SpMV kernel on GPU)
8. Dataset.csv is gathered using the .cu files and used for building ML models.
