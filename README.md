# SYDE-720
Code associated with an evaluation of the method proposed by Mohan et al. (2023) for embedding hard constraints in machine learning models. This method is designed for reconstructing coarse-grained representations of 3-dimensional turbulence. 

I evaluate the impacts of boundary conditions and enforcement of the divergence-free condition for 2-dimensional turbulence, setting the third dimension of the field to 0.

Convolutional autoencoders are compared with and without these conditions. Specifically, five variations of these models were evaluated using total absolute divergence, averaged over the test dataset. Training set size, network layers, kernel size, and loss functions were varied to optimize model performance. Additionally, RMSE was used to evaluate the accuracy of the predictions relative to the original velocity fields. Unknowns from the original study (e.g., model parameters) hinder the ability to directly compare architectures.

Lower total absolute divergence was achieved for the model incorporating hard physical constraints, in line with findings from Mohan et al. (2023). However, lower TAD was sometimes associated with higher losses, resulting in predictions that less accurately reconstruct the original fields. 

---
REFERENCES 
Mohan, A., Lubbers, T., Chertkov, M., & Livescu, D. (2023). Embedding hard physical constraints in neural network coarse-graining for three-dimensional turbulence. Physical Review Fluids, 014604. 
