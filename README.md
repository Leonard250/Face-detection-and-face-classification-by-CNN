FACE RECOGNITION AND FACE VERIFICATION 

This is a readme that shows how to run my program in response to HW2p1 which is about face recognition and face verification using the deep learning model, CNN model. 
It is provided in a single notebook it provides both the best face recognition accuracy and the best face verification accuracy. 
How to run codes
The codes that worked best for face recognition are included in a single notebook so to run the notebook you download it and import 
it on Kaggle or Collab (here you will need to change data file paths) and then turn on GPU(make sure you have enough GPU). Then you click the run all button to run the notebook

Parameters used

we increased the batch size up to 128 since it was the once our GPU could handle, we use learning rate 0.15, more than 100 epochs in different series, at the first we used patience of 3 but we decreased 
it along running process. For the optimizer we used SGD (stochastic gradient descent) with momentum of 0.9 and weight decay of 1e-4. For criterion, we used crossEntropyLoss with smoothing parameter of 0.2.
we also used the scheduler called ReduceLrOnPlateau setting the mode to min with the factor of 0.75 and the patience. GradScaler scaler was also applied. Most importantly, we used some augmentation 
to increase the training data thus to increase the generalizability of  the model thus improving its performance. Those augmentations are randorm perspective, color jitter, random rotation,
random horizontal flip and toTensor as well. We never use augmentation for valid data except if we used normalization as augmentation.

Results

Throughout this notebook I was able to get the best face recognition and face verification accuracy of all the notebook which I attempted in the process. 
In the notebook the best face recognition accuracy was found to be 88.87% and for face verification, the best accuracy was found to be 0.5333 which is equivalent to 53.33%.
on submitting to Kaggle the best face recognition accuracy is 0.8872 and  the best face verification accuracy is 0.50694.
The following graph shows briefly the performance curve of the model. More information can be obtained on the wandb project which is shared via the Google document. 
 

![image](https://github.com/Leonard250/Face-detection-and-face-classification-by-CNN/assets/141337656/94a89873-fc2c-48d9-86a4-cbaa8209df6e)
