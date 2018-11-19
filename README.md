# Auto-encoder for a memoryless fiber-optical channel

This script uses an auto-encoder (AE) for end-to-end learning of a non-linear memoryless fiber channel. The determines a good constellation and a good receiver. The achievable information rate is also computed. 

The system is of the form:
$$
x_{k+1}=x_k \exp (j \gamma L / K |x_k|^2) + n_k, k=0,..,K-1
$$
where $x_0$ is the input (a complex symbol), $\gamma$ is the fiber nonlinearity parameter (typically around 1.2), $L$ is the fiber length, and $K$ is the number of amplification stages. The channel output is $x_K$. Finally, $n_k$ is white Gaussian noise. 


This code was is based on the paper

Shen Li, Christian Häger, Nil Garcia, and Henk Wymeersch, "Achievable Information Rates for Nonlinear Fiber Communication via End-to-end Autoencoder Learning," in *Proc. European Conference on Optical Communication* (2018) [arXiv:1804.07675](https://arxiv.org/pdf/1804.07675.pdf). 

The code was written by Christian Häger. Parts were provided by Shen Li. Integration and polishing by Henk Wymeersch. 

Remaining issues:
*   returns NaN for too high input power
