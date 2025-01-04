# Text-Mining-Assignment01-Sentiment-Analysis-Using-Naive-Bayes
Text-Mining-Assignment01-Sentiment Analysis Using Naive Bayes
Cohort 11 - PGP in AI/ML

C5 - Text Mining

Assignment - Sentiment Analysis Using Naive Bayes 
Perform Text Classification on the data. The tweets related to coronavirus have been pulled from Twitter, and manual tagging has been done. 

You might use some of the References given below:  

1. Sklearn Pipeline

2. Sklearn GridSearchCV

3. ML Pipeline with Grid Search in Scikit-Learn 



Dataset: Coronavirus tweets NLP - Text Classification

 

The steps to be performed are as follows: 
Read dataset and perform Text processing for the tweets ( Remove Stop words, and special characters and convert the text to lowercase) -  1 Mark
Using the train_test_split function of Sklearn, Split the kaggle's train dataset further into train, and test dataset - 1 Mark 
Use BoW and TF-IDF based feature extraction approaches on the "text" field of the dataset. You can use existing library functions. [2+2 marks] 
Create model building pipeline and define parameters for GridSearch (You might Refer to the code below) - 2 Mark 

text_clf = Pipeline([('vect', CountVectorizer()),
                    ('tfidf', TfidfTransformer()),
                    ('clf', MultinomialNB())]) 
 
tuned_parameters = {
                   'vect_ngram_range': [(1, 1), (1, 2), (2, 2)],
                   'tfidf___use_idf': (True, False),
                   'tfidf____norm': ('11', '12'),
                   'clf_alpha': [1, 1e-1, 1e-2]
} 



5. Perform classification (using GridSearch) - 2 Marks 
6. Print the confusion matrix, accuracy, and F1 score on the test dataset - 1 Mark  

7. Interpret your results in terms of Business Domain Knowledge. 1 Mark 



NOTE: 
ALL THE QUESTIONS ARE MANDATORY 
After completing the assignment, you must submit 2 files: the original ipynb file and its HTML version. Both files should have the required outputs (i.e. it should be executed, and outputs should be inline in the ipynb/html file). If outputs are not present, marks will be deducted.
It is your responsibility to ensure the correctness of the HTML/ipynb file uploaded, to ensure all results are visible, the formatting of the file is correct, and to make sure you are not uploading incomplete or older version files. Pay extra attention to verify the formatting of the contents of the converted HTML file.
Do not submit Zip files. 
Explicitly mention the questions as a Markdown cell in your notebook to segregate the different parts that you are attempting. 
No deadline extension would be entertained. We are very strict on this from now on. We really appreciate you starting work on the assignment from Day - 1 to prevent any last-minute occlusions (Health/office work or any other)
