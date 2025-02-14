
How to run the code : 

Download the urban sound 8k dataset in local .
Update the location in training.py like below 

ANNOTATIONS_FILE = 'D:/MTech-BigDataSets/UrbanSound8K/UrbanSound8K/metadata/UrbanSound8K.csv'
AUDIO_DIR = 'D:/MTech-BigDataSets/UrbanSound8K/UrbanSound8K/audio'

Training :  
----------------------------
Open the parameter.py and update the variable for which training is needed

CURREN_WINDOW_FN =torch.hamming_window
run training.py 
It will pick up the windowing we want to use , when the training is completed 
the model will be saved in the saved_model folder like soundclassifier_hamming.pth 

We need to run the training for all three windowing technique to train the model .

Testing and performance metrics 
-------------------------------
run evaluate_performance_all_windowing.py 
This will run the test for all there windowing techniques and capture and calculate 
the performance metrics like accuracy , recall etc. for each of the window techniques.

