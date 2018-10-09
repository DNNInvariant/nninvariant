# NIC and DeepFense

## DeepFense

[DeepFense](https://arxiv.org/pdf/1709.02538.pdf) is published on ICCAD 2018. See the paper for its details.

## Models

The model used by the authors are used to verify the correctness of the implementation.

We use the [Carlini MNIST model](https://github.com/carlini/nn_robust_attacks).

## Results

|  Detector | FP for Carlini Model | FGSM |  BIM | CW Li Next | CW Li LL | DeepFool | CW L2 Next | CW L2 LL | CW L0 Next | CW L0 LL | JSMA Next | JSMA LL | Trojan | FP for LeNet-4 | Dirt | Lighting |  RP  |
|:---------:|:--------------------:|:----:|:----:|:----------:|:--------:|:--------:|:----------:|:--------:|:----------:|:--------:|:---------:|:-------:|:------:|:--------------:|:----:|:--------:|:----:|
| DeepFense |         6.3%         | 100% | 100% |     98%    |    98%   |    93%   |     95%    |    94%   |     88%    |    85%   |    87%    |   88%   |   81%  |      5.2%      |  94% |    99%   | 100% |
|    NIC    |         3.7%         | 100% | 100% |    100%    |   100%   |   100%   |    100%    |   100%   |    100%    |   100%   |    100%   |   100%  |  100%  |      2.5%      | 100% |   100%   | 100% |

## Extra Results

The model used by the authors are used to verify the correctness of the implementation, but we also tested its performance regarding the attacks.

|  Detector |  FP  | FGSM |  BIM | CW Li Next | CW Li LL | DeepFool | CW L2 Next | CW L2 LL | CW L0 Next | CW L0 LL | JSMA Next | JSMA LL | Trojan |
|:---------:|:----:|:----:|:----:|:----------:|:--------:|:--------:|:----------:|:--------:|:----------:|:--------:|:---------:|:-------:|:------:|
| DeepFense | 7.6% | 100% | 100% |     99%    |    99%   |    96%   |     98%    |    98%   |     91%    |    92%   |    90%    |   90%   |   83%  |
|    NIC    | 2.1% | 100% | 100% |    100%    |   100%   |   100%   |    100%    |   100%   |    100%    |   100%   |    100%   |   100%  |  100%  |
