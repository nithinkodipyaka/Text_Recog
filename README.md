# Text_Recog
Text Recognition, CAPTCHA Recognition
*************************************************************************************

The project has been divided into 3 parts: 

1- Captcha Recognition Model

2- Using Googles Tesseract OCR model and Regex to find specific pattern (Registration Number) on a given image file after appropriate cropping.

3- Using the above mentioned Captcha Recognition Model to detect Characters which arent in standard Symbol format for OCR model to recognise.

**************************************************************************************

## For Captcha System:

1- Files can be read as it is from the database and model

2- Preprocessing step takes care of the required image cropping and resizing

3- The input layer will read images of size (50,200)

4- The output layer consists of 6 output nodes which will give the predicition of each character 

Note- Preprocessing step array calculations are set based on the current input. For any other input kindly Preprocess image with properties

GrayScale

tensor of Dtype= float32

Dimensions: (50,200)

**************************************************************************************

## Tesseract:

1- Our task was to find a solution to successfully classify the registration id on Certificates.

2- We used Googles OCR Engine Tesseract for the task.

3- As the position of registration number on the images provided were varying. No fixed Cropping and Resizing step was followed.

4- Images were manually cropped upto the requied position.

Note- Avoid any unnecessary boundaries or texts for best output in the cropped image as the model can bound the borders colour pattern and fail to read the internal content.

***************************************************************************************

## SID Recognition System:

1- Finally our task was to recognise the given SID on the Image file

2- The SID werent in Standard English symbol and misclassified alot when tried to classify with Pytesserect Model.

3- We came up with the solution of using the CNN Model developed for Captcha Classification as its ability to handle distorted texts or pattern for classification

4- The same preprocessing was applied as for Captcha System.

****************************************************************************************

Note- In order to input a test image :
-> Either train the model again or load the weights from previous checkpoint if available

-> In the Encode_single_sample Function replace image path parameter with your image path ( Note- Use "\\" in path instead of "\" )

-> Then input the img numpy array returned to the model.predict() function 

****************************************************************************************


