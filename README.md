Bayesian paramter inference for epithelial mechanics
===

## Description

Here are scripts for Bayesian parameter inference for epithelial mechanics, reported in Yan and Ogita et al. 2024 [1]. 

Using an input file that contains the information about the position and connectivity of cell vertices from an image of epithelial tissue, the scripts can be used to perform non-hierarchical Bayesian parameter inference with **BayesParameterEstimation.py** or hierarchical Bayesian parameter inference with **HBayesParameterEstimation.py**. 

**GetVertex**, a Fiji/ImageJ plug-in for generating an input file from a segmented image, is available from [Github](https://github.com/Sugimuralab/GetVertexPlugin).

## Requirement

* pymc3==3.11.4

* arviz==0.14.0

* scipy==1.9.3

* sparseqr==1.2.1

* theano==1.1.2

## Usage

1. Prepare input files from the same developmental stage in the same format as the attached sample folder (./Samples/*/, where * is the stage name).
2. Change the variable "filename" in BayesParameterEstimation.py to the input file from ./Samples/*/ in step 1, or the variable stage in HBayesParameterEstimation.py to the stage name *.
3. Run "BayesianParameterEstimation.py" or "HBayesianParameterEstimation.py" on IDE or IPython.

These Bayesian parameter inference coded were originally implemented for image datasets of in vivo epithelial tissues. For inference using synthetic data, please set the following flags accordingly:
 - `AreaNormalization = False`  
 - `Artificial = True`

 instead of the default ones:
 - `AreaNormalization = True`  
 - `Artificial = False`

## Reference
1. Xin Yan, Goshi Ogita#, Shuji Ishihara, and Kaoru Sugimura# (2024)<br>
"Bayesian parameter inference for epithelial mechanics."<br> Journal of Theoretical Biology [[https://www.sciencedirect.com/science/article/pii/S0022519324002455](https://www.sciencedirect.com/science/article/pii/S0022519324002455)]

