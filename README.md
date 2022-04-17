# Clothes-Classification
small exercise to classify cloths images by types
the dataset used can be found at [kaggel: clothes types dataset](https://www.kaggle.com/datasets/salil007/caavo)

Note: 
text labels were not included in the dataset docs
only the labeling format was row-index_class-number.jpg
to download the dataset into the colab note you'll need to get a kaggle api key and a kaggle.json file from your kaggle account 


approach :
the approach was to fine tune an image classification model to fit the problem 
as pretrained models have a ready to use feature extractor that was trained on large datasets (ex: image net)
then changing the input and output layers to fit our data 
while trying not to pick models that are too big for the problem (which I might've ended up doing) 
I used python and Keras for the model training and testing 

steps taken :
1. Finding a dataset
      - I browsed thourgh the internet and Kaggle to find a dataset that's useable for this project and found one that was easily accessable , free and had clothing categories 
2. Exploring dataset 
- after finding the dataset I had to explore it to discover its structure 
- the dataset consisted of two main folders ( the train and test folders) 
- the train folder had the class of the image in the imagename 
- the test folder had un labled images in them and so I decided not to use it for the final metrics 
3. setting up repo and colab note 
4. picking models I want to try 
- I decided I wanted a classification model fine tuned to use the already well trained feature extraction back bones of the models 
- after going through lists of classifciation models I chose to start with inceptopn V3 and Resnet50 and go back to alexnet if I get the time 
- (alexnet being picked for an old personal thing)
- and being left behind cause most avalaible weights were in caffe and I decided to use keras really early on as I'm more familiar with it  
5. Downloading data into notebook
6. Data handling
- reading data 
- one hot encoding
- data generator
7. Setting up model training 
- calling resnet50 and inception v3 function in the code 
- removing the input and output layers and adding dense layers that fit my class count 
8. running models training and waiting for the results 



data handling techniques 
resizing data to fit the input shape 

difficulties faced 
with the dataset's total size being less than 700mbs the first approach used was to load the whole dataset 
but the dataset once loaded into ram took up 6GBs which limited the available memory for the training 
the approach of loading the data had to then be changed to using a generator function
