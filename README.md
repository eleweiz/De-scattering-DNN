# De-scattering-DNN
## Configurations: 
**Suggested Environment**: Matlab+Visual Studio Code +Python 3.6.4 +  Tensorflow 2.5；

**Data format**: Set mat version in MATLAB to be 7.3 or higher (On the Home tab, in the Environment section, click Preferences. Select MATLAB > General > MAT-Files.) ；

We offer two examples for demonstration purpose: Toy example and Spine Example. 

## Toy example (MNIST Digit):

![image](https://user-images.githubusercontent.com/47460581/122369265-9cedc300-cf90-11eb-924b-44d95bd7830f.png)

**Figure 1**: The Ground truth is 3D rotated MNIST digit. The input is TFM images generated with the forward solver from Ground truth. Output is the reconstruction from the proposed method.

There are 3 steps in total in this shared code：

**Step 1**. Generate training data with **main_forward.m**: 

**Step 2**. Train the network with **main_inverse.py**：

**Step 3**. Display your results with **Display_Results.py**: Remember to replace the trained model name at Line 25. 


## Spine example:

![image](https://user-images.githubusercontent.com/47460581/122369422-c1499f80-cf90-11eb-86bd-cbf624ab1008.png)

**Figure 2**: The Ground truth is 3D mScarlet-I experimental PSTPM stack. The input is mScarlet-I experimental TFM images. Output is the reconstruction from the proposed method.

**Data downloading**: Download the data from Zenodo: http://doi.org/10.5281/zenodo.4972170 .
Put the two folders, i.e., "PSTPM_data" and "Results", under the path *./Spine_Example*.

To display the results, use **Results_Demo.m**, where we have also offered mScarlet-I experimental results as an example.

There are 3 steps in total in this shared code to train and test the model:

**Step 1**. Generate training data with **main_forward.m**: The PSTPM stack are contained in the "PSTPM_data" folder, where others can put their own PSTPM data in the folder to generate training data.

**Step 2**. Train the network with **main_inverse.py**.

**Step 3**. Test and Save the test results with the file **Save_data.py**: Remember to replace the trained model name at Line 32. 
