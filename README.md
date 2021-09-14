# Neural network modeling of polarization in liquid crystals

This repository provides data and supplementary material to the paper **Deep learning of polarization transfer in liquid crystals with application to quantum state preparation**, preprint: arXiv:21XX.XXXXX [quantum-ph], by Dominik Vašinka, Martin Bielak, Michal Neset, and Miroslav Ježek.

Direct_model.h5
- a file containing a deep neural network built in Keras library with tensorflow backend
- the neural network coresponds to the direct model from section "Direct models and dataset-size scaling"

Compound_model.h5
- a file containing a deep neural network built in Keras library with tensorflow backend
- the network coresponds to the compound model from section "Inverse and compound model"

Dataset_size_scaling.ipynb
- a jupyter notebook for reproducting the Fig. 2: The infidelity dependence on the number of samples in the training set
- requires loading of the following files contained within "Data_files" folder:
    - DNN_all_fidelity_val_tensor_part_1.npy, DNN_all_fidelity_val_tensor_part_2.npy
    - DNN_all_fidelity_test_tensor_part_1.npy, DNN_all_fidelity_test_tensor_part_2.npy
    - LI_all_fidelity_val_tensor_part_1.npy, LI_all_fidelity_val_tensor_part_2.npy
    - LI_all_fidelity_test_tensor_part_1.npy, LI_all_fidelity_test_tensor_part_2.npy
    - RBF_all_fidelity_val_tensor_part_1.npy, RBF_all_fidelity_val_tensor_part_2.npy
    - RBF_all_fidelity_test_tensor_part_1.npy, RBF_all_fidelity_test_tensor_part_2.npy

Evaluation_of_DNN.ipynb
- a jupyter notebook for reproducing the infidelity results of direct and compound deep learning models
- requires loading of models "Direct_model.h5" and "Compound_model.h5", together with following files from "Data_files" folder:
    - training_voltages.npy, validation_voltages.npy, validation_voltages.npy
    - training_rhos.npy, validation_rhos.npy, test_rhos.npy

Evaluation_of_interpolation_methods.ipynb
- a jupyter notebook for reproducing the infidelity results of linear and radial basis function interpolation models
- requires loading of the following files from "Data_files" folder:
    - training_voltages.npy, validation_voltages.npy, validation_voltages.npy
    - training_rhos.npy, validation_rhos.npy, test_rhos.npy

Logo_projection.ipynb
- a jupyter notebook for reproducting the Fig. 5: Palacký University logos on the Bloch sphere
- requires loading of the "Compound_model.h5" file, together with the following files from "Data_files" folder:
    - logo_points_cartesian.npy
    - weak_signal_heralded_stokes.npy
    - entangled_state_density_matrix_MN.npy








