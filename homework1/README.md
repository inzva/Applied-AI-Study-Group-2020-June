# Applied-AI-Study-Group-2020

## Descritions of Homeworks

### Homework 1

- This homework will benefit your data preprocessing skills and model building skills on computer vision. 

- We will take an input image, and detect the "keypoints" in the image. Our dataset consists of hands, and the so called keypoints are the joint locations of the hand. We will regress from the image matrices to the keypoint location vectors.

- Copy-paste is worse than non-submission. (just dont copy paste code that is: written by someone else to do this homework)

- Note that this homework is not a liability, instead it is only to benefit your skills.




Steps:

1- Download this dataset: http://www.rovit.ua.es/dataset/mhpdataset/

2- Dataset will be consisting of images and 3D location coordinate files of the joints. You need to project 3D coordinates into 2D coordinates to make the problem easier for the network. Luckily, dataset publishers provided a conversion script. Script is named: 'generate2Dpoints.py'. You need to run this script and generate txt files for the 2D coordinates. You might encounter some errors, however, help will be provided in the discord group.

3- After projecting 3D coordinates into 2D by running the provided script, you need to generate the bounding box coordinate txt files. The relevant script for this task is named 'generateBBoxes.py'. Again, help will be provided for errors.

4- After creation of the relevant txt files, you need to 'pickle' the dataset. Pickle is a format to save the objects in python. 
	So you need to: 
	
		- read the joint labels and bounding box labels from the text files, 
		- read the image data from .jpg files; 
		- write the image data, bounding box labels and joint coordinate labels in a pickle file.


	Assume you gathered the relevant data in three python objects named: (images, joints, bounding)
	Now you can put them inside a dictionary: mydict = {'images':images,'joints':joints,'bounding':bounding}
	And you can save the dictionary to your computer: 
	
			with open('data_hand_pose.pickle','wb') as file_to_dump:
			    pickle.dump(mydict,file_to_dump)


5- Now you need to preprocess the images. You can do this before saving the pickle file too. 
		
			1- You need to crop each hand image by looking at its bounding box labels
			2- You need to somehow make the cropped image matrices the same size. There are two intuitive ways of this:

				a- Reshape the matrices to a common shape. (there are numpy and other library functions for this)
				b- Pad all the matrices to the: maximum height and maximum width in the dataset

			3- You need to shift the joint coordinate labels according to your preprocessing. When you crop the images, your older joint labels are invalid, you need to calculate the new valid coordinates. The same holds for isometric padding and reshaping.

			4- Ultimately dont forget to check that all image matrices are in the same shape and the joint coordinate labels are in true position (Visualize the labels on the image to check this. You can visualize each joint coordinate as a red dot on the hand image, for example.)


6- Now you need to setup your model. Set a CNN with appopriate hyperparameters to predict the joint coordinates from any image.

7- Test your model in your previously divided test set.

8- Optionally, test your model in a real time environment, for example the webcam of the computer. Check if the model succeeds. What could be the reasons of the model succeeding or not?

    

	


Please submit your homeworks into the repository as:


Please submit your homeworks into the repository as:

	1- form a folder with the names of your team members: person1name_person1surname-'and'-person2name_person2surname
	2- inside the folder put: preprocessing.ipynb
	3- inside the folder put: model.ipynb
	4- load your pickle files into your google drive, copy the share link, share the link in our discord channel.


