# TF_CNN_IEEG
Intracranial EEG (iEEG) Pattern Recognition with Convolutional Neural Network in TensorFlow.
These scripts generate Z-normalized spectrograms from iEEG data at time bins T for each channel C in an electrode grid with size width x depth (W x D). 
The spectra are frequency binned into F frequencies to create tensors with dimension (W x D x F) for use with CNN, e.g. AlexNet used here as a toy example. 


prep_data_v1_20180915.ipynb contains pre-processing functions for EEG data in HDF5 files with structure (channel x time sample)

tf_cnn_dev.py contains neural network architecture and training code
