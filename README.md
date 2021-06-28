# Check-Material-Type-Using-ThermalSensing

The above repository takes thermal videos as input, and outputs a class to which the material, whose thermal sensing is done belongs to. The data collection was done on three materials - Coffee  Cup (Class 0), Plastic Bottle (Class 1) and Ciggrette butt (Class 2). 

## **Repository Structure**

The repository contains the following folders:

- Data: Contains data of all the three materials in Natural Hold (19 samples), Fixed Hold (19 samples) and Combined (data of both fixed hold and natural hold) in .npz format
- Training Data: Contains combined data of all materials of fixed Hold, Natural Hold and Mixed or Combined Hold in .npz file format to be used for training the models.
- Notebooks: The notebooks contain code files 
  - datapreprocessingandnormalisation.ipynb
  - Training Folder, wherein you can find the training model code for fixed hold, natural hold and combined hold.
  - prediction.ipynb
- saved models: The trained models are saved in this folder. There are 3 saved models in this folder - fixed hold, natural hold and combined hold.

## A PEEP INSIDE THE REPOSITORY:

The training process is done and the models for Fixed Hold, Natural Hold and Combined are saved in saved models folder with an accuracy of 72% (on test data). Still if you wish to enhance the model or train the model with more data and also find any other classifier more suited for the classification then follow the steps below:

- Download the whole repository
- The model uses Thermal Videos for training and prediction. 
- open the *dataprocessingandnormalisation.ipynb* and add the input location of the video and also the output location, where you wish to store the extracted frames. 
- update the other foldr locations in the code too.
- Once .npz files are created for the thermal videos the data is set to be given as input to the training.
- I have used random forest for the training.
- The models for fixed hold, natural hold and combined (mixed) are saved using ***pickle***

## HOW TO USE THE MODEL FOR PREDICTION:

- If you just want to use the model for prediction, just download the *prediction.ipynb* and also the *saved models*
- Update the location of the video and also other locations which need access to your local machine.
- The Folders like ***frames*** (to store the extracted frames) and ***step2*** (to store the segmented binary images) need to be created. Or you can also use any name but it needs to be updated in the code


## HOW TO INTERPRET THE OUPUT:

- Class 0 means Coffee Cup
- Class 1 means Plastic Bottle
- Class 2 means Ciggerette Butt

