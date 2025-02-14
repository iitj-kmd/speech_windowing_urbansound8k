# Experiment with Windowing Techniques with Urban Sound 8K dataset 
Experiments with Hann , Hamming and Rectangular Windowing Techniques on Sound classification</br>
on Urban Sound Dataset</b>

How to run the code : </br>
- Download the urban sound 8k dataset in local . </br>
- Update the location in training.py like below  </br>
- ANNOTATIONS_FILE = 'D:/MTech-BigDataSets/UrbanSound8K/UrbanSound8K/metadata/UrbanSound8K.csv' </br>
- AUDIO_DIR = 'D:/MTech-BigDataSets/UrbanSound8K/UrbanSound8K/audio' </br>

Training :  </b>
- Open the parameter.py and update the variable for which training is needed </br>
- CURREN_WINDOW_FN =torch.hamming_window  </br>
- run training.py  </br>
```
python train.py
```
- It will pick up the windowing we want to use , when the training is completed  </br>
the model will be saved in the saved_model folder like soundclassifier_hamming.pth  </br>
- We need to run the training for all three windowing technique to train the model . </br>

Testing and performance metrics </b>
- run evaluate_performance_all_windowing.py  </br>
```
python evalute_performance_all_windowing.py
```
- This will run the test for all there windowing techniques and capture and calculate  </br>
- the performance metrics like accuracy , recall etc. for each of the window techniques.  </br>

