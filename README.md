# Computer-Vision

Part A - 20 Marks

DOMAIN: Entertainment
• CONTEXT: Company X owns a movie application and repository which caters movie streaming to millions of users who on subscription basis.
Company wants to automate the process of cast and crew information in each scene from a movie such that when a user pauses on the movie
and clicks on cast information button, the app will show details of the actor in the scene. Company has an in-house computer vision and
multimedia experts who need to detect faces from screen shots from the movie scene.
The data labelling is already done. Since there higher time complexity is involved in the
• DATA DESCRIPTION: The dataset comprises of images and its mask for corresponding human face.
• PROJECT OBJECTIVE: To build a face detection system.
Steps and tasks: [ Total Score: 20 Marks]

1. Import and Understand the data [7 Marks]
   A. Import and read ‘images.npy’. [1 Marks]
   B. Split the data into Features(X) & labels(Y). Unify shape of all the images. [3 Marks]
   Imp Note: Replace all the pixels within masked area with 1.
   Hint: X will comprise of array of image whereas Y will comprise of coordinates of the mask(human face). Observe: data[0], data[0][0], data[0][1].
   C. Split the data into train and test[400:9]. [1 Marks]
   D. Select random image from the train data and display original image and masked image. [2 Marks]
2. Model building [11 Marks]
   A. Design a face mask detection model. [4 Marks]
   Hint: 1. Use MobileNet architecture for initial pre-trained non-trainable layers.
   Hint: 2. Add appropriate Upsampling layers to imitate U-net architecture.
   B. Design your own Dice Coefficient and Loss function. [2 Marks]
   C. Train and tune the model as required. [3 Marks]
   D. Evaluate and share insights on performance of the model. [2 Marks]
3. Test the model predictions on the test image: ‘image with index 3 in the test data’ and visualise the predicted masks on the faces in the image. [2 Marks]

Part B - 10 Marks

DOMAIN: Entertainment
• CONTEXT: Company X owns a movie application and repository which caters movie streaming to millions of users who on subscription
basis. Company wants to automate the process of cast and crew information in each scene from a movie such that when a user pauses on
the movie and clicks on cast information button, the app will show details of the actor in the scene. Company has an in-house computer
vision and multimedia experts who need to detect faces from screen shots from the movie scene.
The data labelling is already done. Since there higher time complexity is involved in the
• DATA DESCRIPTION: The dataset comprises of face images.
• PROJECT OBJECTIVE: To create an image dataset to be used by AI team build an image classifier data. Profile images of people are given.
Steps and tasks: [ Total Score: 10 Marks]

1. Read/import images from folder ‘training_images’. [2 Marks]
2. Write a loop which will iterate through all the images in the ‘training_images’ folder and detect the faces present on all the images. [3 Marks]
   Hint: You can use ’haarcascade_frontalface_default.xml’ from internet to detect faces which is available open source.
3. From the same loop above, extract metadata of the faces and write into a DataFrame. [3 Marks]
4. Save the output Dataframe in .csv format. [2 Marks]

Part C - 30 Marks

DOMAIN: Face Recognition
• CONTEXT: Company X intends to build a face identification model to recognise human faces.
• DATA DESCRIPTION: The dataset comprises of images and its mask where there is a human face.
• PROJECT OBJECTIVE: Face Aligned Face Dataset from Pinterest. This dataset contains 10,770 images for 100 people. All images are taken
from 'Pinterest' and aligned using dlib library. Some data samples:
Steps and tasks: [ Total Score: 30 Marks]

1. Unzip, read and Load data(‘PINS.zip’) into session. [2 Marks]
2. Write function to create metadata of the image. [4 Marks]
   Hint: Metadata means derived information from the available data which can be useful for particular problem statement.
3. Write a loop to iterate through each and every image and create metadata for all the images. [4 Marks]
4. Generate Embeddings vectors on the each face in the dataset. [4 Marks]
   Hint: Use ‘vgg_face_weights.h5’
5. Build distance metrics for identifying the distance between two similar and dissimilar images. [4 Marks]
6. Use PCA for dimensionality reduction. [2 Marks]
7. Build an SVM classifier in order to map each image to its right person. [4 Marks]
8. Import and display the the test images. [2 Marks]
   Hint: ‘Benedict Cumberbatch9.jpg’ and ‘Dwayne Johnson4.jpg’ are the test images.
9. Use the trained SVM model to predict the face on both test images. [4 Marks]
