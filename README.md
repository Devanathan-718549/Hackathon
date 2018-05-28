# Hackathon
Creating Hackathon for Machine Learning
Hackathon Medical Insurance Claim

1)What is it ?
Fraudulent medical insurance claim - Developed system which is trained with models containing 36 data. These data train the application to detect whether a claim is fraud or non fraudulent.

Prerequisite
------------
.)Anaconda 1.7.0 or latest version recommended, use spyder IDE for running the python files


Files
-----
.)TD1.csv - contains the training data model used to train the machine learning application
.)Properties.ini - contains the path of training model data and user input data to be loaded & validation index
.)UserInput.csv - contains the user input data to be validated
.)Hackathon.py - contains the logic detect the claim provided  by the user is valid or not based on the KNN,LogisticRegression,LinearDiscriminantAnalysis,DecisionTreeClassifier,GaussianNB,SVC algorithm

Assumptions
-----------
.) Both Training data file (TD1.csv) column length and UserInput file (USerInut.csv) column length should be same length and in the same format
.) Training Data Description
	.) Gender - 1 - Female, 2 - Male
	.)Age - age of the person admitted
	.) Amount - amounts divided by 1 lakh eg. 50000 represented as 0.5;
	.)ClaimType- contains values like Maternity(1),Accident(3)
	.)InsuranceClass - Classified as 1,3 based on the coverage he has applied eg)1 lakh coverage, 5 lakh coverage
	.)Class - 1- Not Fraud , 0 - Fraud
.) The number of columns in both Training data and User input is dynamic except the last column should be our deciding result i.e target attribute

Working
-------
.) Initially properties.ini file is loaded to fetch the file paths for training model and user input model . 
	Contents in INI file
	--------------------
	.)filePath - path to training data is provided here(TD1.csv)
	.)userInputFilePath - path to user input data is provided here(UserInput1.csv)
.) Initialize the fetched training model data from TD1.csv datavalues to an array 
.) Initialize the fetched user input data from UserInput1.csv userInputArray to an array
.) Created training x and y using datavalues array
.) Created validation/ test data x and y using userInputArray array
.) Apply corresponding algorithms and accuracy , prediction results are identified for each algorithm used 
	
	
	
Future Expansions
-----------------
.)Creating a rest endpoint service on google cloud to accept the claim data as user input and process it via ml system to check if claim is fraud or non fraud	
