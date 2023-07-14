# diff-fdn-colorless
Demo for the differentiable feedback delay network (FDN) for colorless reverberation submitted to the 26th International Conference on Digital Audio Effects (DAFx 2023). 
## Overview 
In this work we introduce an optimization framework to tune a set of FDN parameters (feedback matrix, input gains, and output gains) to achieve a smoother and less colored reverberation. 
## Abstract 
Artificial reverberation algorithms often suffer from spectral coloration, usually in the form of metallic ringing, which impairs the perceived quality of sound. This paper proposes a method to reduce the coloration in the feedback delay network (FDN), a popular artificial reverberation algorithm. An optimization framework is employed entailing a differentiable FDN to learn a set of parameters decreasing coloration. The optimization objective is to minimize the spectral loss to obtain a flat magnitude response, with an additional temporal loss term to control the sparseness of the impulse response. The objective evaluation of the method shows a favorable narrower distribution of modal excitation while retaining the impulse response density. The subjective evaluation demonstrates that the proposed method lowers perceptual coloration of late reverberation, and also shows that the suggested optimization improves sound quality for small FDN sizes. The method proposed in this work constitutes an improvement in the design of accurate and high-quality artificial reverberation, simultaneously offering computational savings.

## Getting started 
To install the required packages using conda environments open the terminal at the repo directory and run the following command
```
conda env create -f colorless-fdn.yml
```
The optimization is coded in Pytorch. Set the configuration parameters in `config.py` and launch the training by running `solver.py`. The initial and optimized parameters values are saved in `output/.`.

The repository also contains a MATLAB demo `demo.m` that shows how to load the model parameters in matlab and uses Sebastian Schlecht's [fdnToolbox](https://github.com/SebastianJiroSchlecht/fdnToolbox) to compute the impulse response and modal decomposition. 

## References
Audio demos are published in: [Differentiable Feedback Delay Network for Colorless Reverberationg](http://research.spa.aalto.fi/publications/papers/dafx23-colorless-fdn/).  
If you would like to use this code, please cite the related DAFx conference paper (submitted) using the following reference:
```
Dal Santo Gloria, Karolina Prawda, Sebastian J. Schlecht, and Vesa Välimäki. "Differentiable Feedback Delay Network for colorless reverberation." International Conference on Digital Audio Effects (DAFx23), Copenhagen, Denmark, Sept. 4-7 2023 
```
