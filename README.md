# Micro-Pi
A small program that aims to calculate millions of digits of pi using the Chudnovsky algorithm: 
![image](https://user-images.githubusercontent.com/39564012/133270538-0f86afee-129d-47d8-82f8-54bdb72bd994.png)

Binary splitting is used to speed up the calculation of the sum of these rational terms. 

Normally multiplication of n-digit integers takes O(n^2) time, however using algorithms different algorithms, the time complexity can be significantly reduced. Some algorithms include Karatsuba multiplication = 0( n^~1.59 ) and FFT multiplication which can be as low as O( n log(n) ).

CUDA supports FFT, so FFT, inverse FFT, and pointwise multiplication are implemented on the GPU.

Note: This a fun project not designed for absolute speed & optimization. It is several orders of magnitude slower than [y-cruncher](http://www.numberworld.org/y-cruncher/).


## TODO
- CUDA supports 32-bit multiplication - use base 4294967295 (unsigned 32 bit int) instead of base 10
- 


## Useful links & references:

- Theory and time complexity: http://www.cecm.sfu.ca/organics/papers/borwein/paper/html/node11.html
- More theory and time complexity: http://numbers.computation.free.fr/Constants/Algorithms/fft.html
- Basic algorithm in python: https://www.craig-wood.com/nick/articles/pi-chudnovsky/
- CUDA accelerated Multiple Precision Arithmetic library: https://github.com/NVlabs/CGBN
- CUDA FFT accelerated integer multiplication: https://github.com/Alexhaoge/FFT-MPI-OpenMP-CUDA
- Karatsuba  multiplication: https://pythonandr.com/2015/10/13/karatsuba-multiplication-algorithm-python-code/
- Mini-Pi (basic version of y-cruncher): https://github.com/Mysticial/Mini-Pi
