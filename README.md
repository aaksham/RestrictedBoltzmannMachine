# RestrictedBoltzmannMachine

- rbm_es.m: Implementation of restricted boltzmann machine using the contrastive divergence algorithm for training.
- rbm_es_kCD.m: Implementation of RBM with varying steps of gibbs sampling while training using contrastive divergence.
- sampling.m: Generating images from the trained RBM.
- backprop_sgd_momentum_l2reg.m: Feedforward neural network trained using stochastic gradient descent initialized with weights pre-trained using an RBM.
- autoencoder.m: Learning the generative distribution of the RBM using an autoencoder
- denoise_autoencoder.m: Denoised version of the autoencoder.


All models employ the early stopping criteria of stopping when the validation error does not decrease. This criteria can be relaxed or tightened in all model files by adjusting the parameter 'early_stopper_limit' which will allow the validation error to increase 'early_stopper_limit' times before stopping.

-All the parameter configurations can be adjusted at the beginning of the model files.

-Each model file also generates 3 files: 
	-The training and validation error trace in a csv file named with the details of the parameters
	-The best learned weights in the training round
	-The image of the visualized best learned weights before early stopping
