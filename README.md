# AI101-Mini-project
## Movie recommender 
## Group-44
## Team Members

| S. No. | Name | Entry Number | Role |
|:------:|---|:---:|---|
| 1 | Aadarsh Kumar | 2026EEB1309 | Execution Lead |
| 2 | Ankush Chaudhary | 2026AIB1017 | Documentation Lead |
| 3 | Aryan Rahul Bachchhav | 2026MCB1517 | Video Lead |
| 4 | Abhinav Mishra | 2026DAB1289 | PPT Lead |

# Video link 
https://drive.google.com/file/d/1melYS94lkLpGG8LC6oobDpV6RxrR1_2h/view?usp=drivesdk

# 1. Installing the required libraries
The required Python libraries are installed and imported. Pandas and NumPy are used for handling data and calculations, while Matplotlib and Seaborn are used for graphs. Scikit-learn is used for machine learning and model evaluation.
# 2. importing the libraries
The current working directory is checked to make sure Python is using the correct folder for the project files and dataset.
# 3. Loading Data from CSV File
The Netflix dataset is loaded using Pandas. Basic information such as the first five rows using df.head(), dataset shape, column names and data types is checked to understand the dataset
# 4. Explaining the data
The dataset is analysed to find statistical information, missing values, duplicate records, content type distribution and the most common genres.
# 5. Data preprocessing
The data is cleaned before using it for analysis and machine learning. Duplicate records are removed, important missing values are handled, text values are cleaned and release year and duration are converted into useful numerical values.
# 6. Statistical information of data
Statistical measures such as mean, median, standard deviation and variance are calculated. Movie duration is analysed separately because TV Show duration is represented in seasons. Covariance and correlation are also calculated.
# 7. Getting knowledge about what Genre the person likes
The genres in the listed_in column are separated and converted into numerical features. MultiLabelBinarizer is used so that each genre can be represented using 0 and 1.
# 8. Checking Correlation
The content type is converted into binary form, where Movie is represented by 1 and TV Show by 0. Correlation and covariance are calculated to understand the relationship between genres, release year and content type. A heatmap is also created for visualization.
# 9. Analysing Features
The input features are stored in X and the target variable is stored in y. Movie is represented as 1 and TV Show as 0. SelectKBest with the Chi-Square test is used to select the most useful features.
# 10. Data Splitting
The dataset is divided into training and testing data. 80% of the data is used for training and 20% is used for testing. The testing data is kept separate so that the model can be evaluated on unseen data.
# 11. Feature Selection
The best features are selected using SelectKBest. Feature selection is performed after splitting the data so that information from the testing data does not affect the training process.
# 12. Normalization
StandardScaler is used to scale the selected features. The scaler is fitted using the training data and then applied to the testing data.
# 13. Logistic Regression and Training of Model
A Logistic Regression model is created and trained using the selected and scaled training data. The model learns to classify each title as either a Movie or a TV Show.
# 14. Testing of model
The trained model is used on the testing data to make predictions. The model also gives probabilities for its predictions.
# 15. Metrics Evaluation
The model is evaluated using Accuracy, Precision, Recall, F1 Score, RMSE and ROC-AUC. These measures help us understand how well the model is performing.
# 16. Confusion Matrix Creation
A confusion matrix is created to compare the actual values with the predicted values. It shows the correct and incorrect predictions for Movies and TV Shows.
# 17. Data Visualization And Model Plots
Different graphs are created to understand the dataset and model. These include Movies vs TV Shows, release year distribution, most common genres, Logistic Regression coefficients and the ROC curve.
# 18. Movie Recommendation
The recommendation system considers only movies and compares their genres. A similarity score is calculated between the selected movie and other movies
# 19. Testing The Recommendation System
The user provides a movie name and the system finds movies with similar genres. The movies are sorted according to their similarity score and the most similar movies are recommended.










