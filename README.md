# Logit_Uncertainty
Logit Uncertainty for deep learning classification

Code is organized as follows:
- Class to compute uncertainty
- Usage example using MNIST
  - Create and train model on MNIST
    - The model should support model.predict() function, and the return of model.predict() should be logit values (not softmax probabilities)
  - Using the logit_uncertainty class
    - The default way to create a logit_uncertainty instance requires selecting number of components for Gaussian Mixtures for each class, this might be a very slow process especially if the data have many classes. However, empirically, number of components for each class are similar to each other. So one way around this is select number of components based on a few classes, and set number of components equal for all classes
    - The plot used to select number of components shows BIC for 1-20 components, however, you can change the n_components to show more components (Have never encountered this case before). 
  - Testing on out of sample examples
  - Testing on MNIST using different assumptions
    - requirement: q1 > q2, then u1 > u2. One can start with default value, and test a few different assumptions, find assumption that suits your need
