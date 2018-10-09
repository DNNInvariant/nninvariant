
# Attack Parameters

## Goal

The experiments try to study the effects of using NIC to detect adversarial samples on various attack parameters.

## Models and attacks

The experiments are done on the MNIST dataset using the cleverhans model (without adversarial training). The parameters are the ones may affect the quality of the attacks.

## FGSM

* EPS: float, maximum distortion of adversarial example compared to original input

|       EPS      | 0.05 |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |
|:--------------:|:----:|:----:|:----:|:----:|:----:|:----:|
| Detection Rate | 100% | 100% | 100% | 100% | 100% | 100% |
| False Positive |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |

## BIM

* EPS: float, maximum distortion of adversarial example compared to original input
* EPS_Iter: float, step size for each attack iteration

###### Detection Rate

| EPS-Iter\EPS | 0.05 |  0.1 |  0.2 |  0.3 |  0.4 |  0.5 |
|:------------:|:----:|:----:|:----:|:----:|:----:|:----:|
|     0.01     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.02     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.03     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.04     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.05     | 100% | 100% | 100% | 100% | 100% | 100% |

###### False Positive Rate

| EPS-Iter\EPS | 0.05 | 0.1 | 0.2 | 0.3 | 0.4 | 0.5 |
|:------------:|:----:|:---:|:---:|:---:|:---:|:---:|
|     0.01     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.02     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.03     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.04     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.05     |  0%  |  0% |  0% |  0% |  0% |  0% |

## JSMA

* theta: float, perturbation introduced to modified components (can be positive or negative)
* gamma: float, maximum percentage of perturbed features

###### Detection Rate

| gamma\theta  | -0.1 |  0.1 |  0.5 |  1.0 |  1.5 |  2.0 |
|:------------:|:----:|:----:|:----:|:----:|:----:|:----:|
|     0.01     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.05     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.10     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.15     | 100% | 100% | 100% | 100% | 100% | 100% |
|     0.20     | 100% | 100% | 100% | 100% | 100% | 100% |

###### False Positive Rate

| gamma\theta  | -0.1 | 0.1 | 0.5 | 1.0 | 1.5 | 2.0 |
|:------------:|:----:|:---:|:---:|:---:|:---:|:---:|
|     0.01     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.05     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.10     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.15     |  0%  |  0% |  0% |  0% |  0% |  0% |
|     0.20     |  0%  |  0% |  0% |  0% |  0% |  0% |


## CW2

* Con: int, confidence of the generated adversarial sample to fool the network

Other const parameters for this attack:

* Batch size: 1
* Learning rate: 0.01
* Binary search steps: 9
* Max iteration: 1000
* Abort early: true
* Initial const: 0.001

|       Con      |   0  |  10  |  20  |  30  |  40  |  50  |  60  |  70  |  80  |  85  |
|:--------------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| Detection Rate | 100% | 100% | 100% | 100% | 100% | 100% | 100% | 100% |  97% |  95% |
| False Positive |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |  0%  |

## DeepFool

| c\iter |   5  |  10  |  20  |  50  |  100 |
|:------:|:----:|:----:|:----:|:----:|:----:|
|  0.001 | 100% | 100% | 100% | 100% | 100% |
|  0.002 | 100% | 100% | 100% | 100% | 100% |

| c\iter |  5 | 10 | 20 | 50 | 100 |
|:------:|:--:|:--:|:--:|:--:|:---:|
|  0.001 | 0% | 0% | 0% | 0% |  0% |
|  0.002 | 0% | 0% | 0% | 0% |  0% |
