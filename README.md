# Gesture_Recognition_Assignment
Gesture_Recognition_Assignment as part of PG Diploma in DS,ML and AI


Experiment Number	Model	Result 	Decision + Explanation
1	Conv3D	Lot of data so unzipped data in my google rive and mounted it.	Direct copy of data was failing hence had to unzip to google drive and mounted google drive so that data will be available and wont be lost once session changes
2	Conv3D	Throws Generator error –“Input to reshape is a tensor with 294912 values, but the requested shape requires a multiple of 12800”	1.	This error was coming when dimension of images I kept as 100x100 . Error got resolved Resized images with 84x84 dimension 
2.	Also applied min max normalization 
3	Conv3D	Experimented with model 1 of 3 Conv3D layer which has 4 filters -32,32,64,64 , Kernel size- (3,3,3 ) respectively , and batch normalization but model accuracy results were not promising.
Below is model summary for model 1 
Total params: 1,838,565
Trainable params: 1,838,181
Non-trainable params: 38
	Removed this model1 and tried with another model 2 (explained in row 4 below). Removed this because model performance in terms of accuracy was not good. Best saved model .h5 was having training accuracy as 0.6 and validation accuracy as 0.18
4	Conv3D	Model 2 is selected as final model with 3 conv3d 
Filters as 8 , 16,32 and 
Kernel size as (5,5,5),(3,3,3),(1,3,3)

Model Summary as 
Total params: 839,157
Trainable params: 839,093
Non-trainable params: 64

Validation Accuracy – 0.68	Model 1 was not performing good with this model parameters got good performance and training accuracy is 97% , validation accuracy is 68%
5	Conv2D+GRU	ModelGRU with model summary as below 

Total params: 6,294,565
Trainable params: 6,294,565
Non-trainable params: 0


Very poor results coming with this model1 . Training accuracy and validation accuracy were not good




Best saved result was as below 
Training accuracy – 0.21
Validation Accuracy – 0.40	Dropped this model 1 and experimented with model 2 (explained in row 6 below)
6	Conv2D+GRU	ModelGRU 2 with below summary 
Total params: 302,869
Trainable params: 302,741
Non-trainable params: 128

Best saved .h5 has below accuracy 
Training accuracy -  1.00
Validation accuracy – 0.73
	Comparing all other models including conv3d , this model performed better. 
Final Model	Conv2D+GRU ModelGRU2	Best saved .h5 has below accuracy 
Training accuracy -  1.00
Validation accuracy – 0.73

“model-00024-0.00130-1.00000-0.85996-0.73000.h5"

	Final Selected model due to performance



