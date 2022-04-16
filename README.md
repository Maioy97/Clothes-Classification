# Clothes-Classification
small exercise to classify cloths images by types
the dataset used can be found at [kaggel: clothes types dataset](https://www.kaggle.com/datasets/salil007/caavo)

Note: 
text labels were not included in the dataset docs
only the labeling format was <row_index>_<classnumber>.jpg
to download the dataset into the colab note you'll need to get a kaggle api key and a kaggle.json file from your kaggle account 

steps taken :
1. finding a dataset
2. exploring dataset 
3. setting up repo and colab note 
4. picking models I want to try 
5. downloading data into notebook
6. data handling
7. setting up model training 
8. training model 1 
9. training model 2 
10. comparison of results  
11. writing differences 

approach :
the approach was to fine tune an image classification model to fit the problem 
as pretrained models have a ready to use feature extractor that was trained on large datasets (ex: image net)
then changing the input and output layers to fit our data 
I used python and Keras for the model training and testing 

data handling techniques 
resizing data to fit the input shape 

difficulties faced 
with the dataset's total size being less than 700mbs the first approach used was to load the whole dataset 
but the dataset once loaded into ram took up 6GBs which limited the available memory for the training 
the approach of loading the data had to then be changed to using a generator function