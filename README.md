# TF_CNN_IEEG
Intracranial EEG (iEEG) Pattern Recognition with Convolutional Neural Network in TensorFlow.
These scripts generate Z-normalized spectrograms from iEEG data at time bins T for each channel C in an electrode grid with size width x depth (W x D). 
The spectra are frequency binned into F frequencies to create tensors with dimension (W x D x F) for use with CNN, e.g. AlexNet used here as a toy example. 


prep_data_v1_20180915.ipynb contains pre-processing functions for EEG data in HDF5 files with structure (channel x time sample)

tf_cnn_dev.py contains neural network architecture and training code

## System Requirements
matplotlib==2.2.2, pandas==0.22.0, scipy==1.1.0, hickle==2.1.0, pyEDFlib==0.1.9, h5py==2.6.0, numpy==1.13.3, six==1.11.0, scikit_learn==0.19.2, tensorflow==1.10.1

Wavelet Analysis Code by Evgeniya Predybaylo: 
"Python wavelet software provided by Evgeniya Predybaylo based on Torrence and Compo (1998) and is available at URL: 
http://atoc.colorado.edu/research/wavelets/"

Wavelet Z-normalization Routine is based on method by Roehri et al.  
Roehri N, Lina J-M, Mosher JC, Bartolomei F, Benar C-G. Time-frequency strategies for increasing high-frequency oscillation detectability in intracerebral EEG. IEEE Trans Biomed Eng 2016;63:2595–606.
