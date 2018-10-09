# DNN Invariant

This is the repository for our DNN Invariant project.

## Repo Structure

* **fps.md**: examples of natural inputs that are mis-classified as adversarial samples by our trained detector
* **results.md**: results of using different attack parameters to evaluate the strength of our method
* **deepfense**: the implementation of the [DeepFense paper](https://arxiv.org/pdf/1709.02538.pdf) and the performance comparison with our approach. If you are interested, please also check their original [Github repo](https://github.com/Bitadr/DeepFense). It does not contain the source code but the compiled python bytecode files.
* **Models**: code used to train the models
* **data**: adversarial samples used in our evaluation and some trained models in h5 format
