# CGCNN-project-codes-and-dataset

The CGCNN Model is a Crystal Graph Convolutional Neural Network model designed by Tian Xie under Prof. Jeffrey Grossman.
This Model helps predict properties of any material by looking at its crystal structure.

I have used this model to work on my own project to see how well the model can predict band gap for different types of materials and ranges of data.
I also worked on changing certain input parameters to see how the model predictions are affected.

Getting the data and filetring it:(Present in the Dataset collection and distribution file)

Training any Machine Learning Model requires large sets of input data and hence I queried Materials Project website by using their API.
Initially I queried the data for 20000 oxides between the band gap range of 1 - 6 eV and trained the model on it and plot its Mean Absolute Error.
All the experiments conducted and the MAE analyzed throughout the project were for the band gap property only.
The distribution of the data is also written in the codes.
I further filtered the data and removed all the non metallic materials. This left me with a dataset of 4388 elements consisting only of Metallic Oxides.
Any experiment from here on out I used the above dataset of 4388 materials, since its a more focused dataset.

Changing input parameters:

-->One of the experiments conducted on the dataset was on the epochs (Present in the Epochs Experiment File)
I varied the epochs of the model from 15 to 50 with a difference of 5 epochs each time and ran the training of the model 3 times. The MAE of the training set was analyzed for all 3 runs of all epochs and mean was plotted

-->Second experiment on feature vectors:(Present in the Feature Vector Experiment File)
Feature vectors consist of the properties of each element. The vectors in the atom_init file were removed for each property one at a time and the training error of the model was analyzed.
