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
<h2>Dataset Description</h2>

<p>
  The project uses the <b>Netflix Movies and TV Shows Dataset
  (<code>netflix_titles.csv</code>)</b>, which contains information
  about movies and television shows available on Netflix.
</p>

<h3>Dataset Statistics</h3>

<ul>
  <li><b>Total Rows:</b> 6,234</li>
  <li><b>Total Columns:</b> 12</li>
  <li><b>Dataset Source:</b> Kaggle</li>
  <li>
    <b>Dataset Link:</b>
    <a href="https://www.kaggle.com/code/abhichoudhury/a-simple-movie-recommender?select=netflix_titles.csv">
      Netflix Titles Dataset - Kaggle
    </a>
  </li>
</ul>

<h3>Attributes Description</h3>

<table>
  <thead>
    <tr>
      <th>Attribute</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>show_id</code></td>
      <td>Unique identification number assigned to each title.</td>
    </tr>
    <tr>
      <td><code>type</code></td>
      <td>Specifies whether the content is a Movie or TV Show.</td>
    </tr>
    <tr>
      <td><code>title</code></td>
      <td>Name of the movie or television show.</td>
    </tr>
    <tr>
      <td><code>director</code></td>
      <td>Name of the director responsible for the title.</td>
    </tr>
    <tr>
      <td><code>cast</code></td>
      <td>Names of actors and actresses featured in the title.</td>
    </tr>
    <tr>
      <td><code>country</code></td>
      <td>Country where the movie or show was produced.</td>
    </tr>
    <tr>
      <td><code>date_added</code></td>
      <td>Date when the title was added to Netflix.</td>
    </tr>
    <tr>
      <td><code>release_year</code></td>
      <td>Year in which the movie or show was released.</td>
    </tr>
    <tr>
      <td><code>rating</code></td>
      <td>Content classification based on audience suitability.</td>
    </tr>
    <tr>
      <td><code>duration</code></td>
      <td>Running time of a movie or number of seasons of a TV show.</td>
    </tr>
    <tr>
      <td><code>listed_in</code></td>
      <td>Genres or categories associated with the title.</td>
    </tr>
    <tr>
      <td><code>description</code></td>
      <td>Brief summary of the movie or television show.</td>
    </tr>
  </tbody>
</table>

<h3>Dataset Usage</h3>

<p>
  The dataset is used for data analysis, preprocessing, feature selection,
  and identifying similarities between movies based on their genres
  and other relevant attributes to generate movie recommendations.
</p>
<h2>Project Workflow</h2>

<h3>1. Installing the Required Libraries</h3>
<p>
The required Python libraries are installed and imported. Pandas and NumPy are used for data handling and calculations, Matplotlib and Seaborn for data visualization, and Scikit-learn for machine learning and model evaluation.
</p>

<h3>2. Importing the Libraries and Checking Directory</h3>
<p>
The required libraries are imported into the Python environment. The current working directory is checked to ensure that Python is accessing the correct project folder and dataset files.
</p>

<h3>3. Loading Data from CSV File</h3>
<p>
The Netflix dataset is loaded using Pandas. Basic information, including the first five rows using <code>df.head()</code>, dataset shape, column names, and data types, is examined to understand the structure of the dataset.
</p>

<h3>4. Understanding and Explaining the Data</h3>
<p>
The dataset is explored to identify statistical information, missing values, duplicate records, content type distribution, and the most common genres.
</p>

<h3>5. Data Preprocessing</h3>
<p>
The dataset is cleaned before performing analysis and machine learning. Duplicate records are removed, important missing values are handled, text values are cleaned, and release year and duration are converted into useful numerical values.
</p>

<h3>6. Statistical Information of Data</h3>
<p>
Statistical measures such as mean, median, standard deviation, and variance are calculated. Movie duration is analysed separately because TV Show duration is represented in seasons. Covariance and correlation are also calculated to understand relationships between numerical variables.
</p>

<h3>7. Understanding Genre Preferences</h3>
<p>
The genres available in the <code>listed_in</code> column are separated and converted into numerical features. <code>MultiLabelBinarizer</code> is used to represent each genre in binary form (0 and 1).
</p>

<h3>8. Checking Correlation</h3>
<p>
The content type is converted into binary form, where Movie is represented by 1 and TV Show by 0. Correlation and covariance are calculated to understand the relationships between genres, release year, and content type. A heatmap is also created for visualization.
</p>

<h3>9. Analysing Features</h3>
<p>
The input features are stored in <code>X</code> and the target variable is stored in <code>y</code>. Movie is represented as 1 and TV Show as 0. <code>SelectKBest</code> with the Chi-Square test is used to identify the most useful features.
</p>

<h3>10. Data Splitting</h3>
<p>
The dataset is divided into training and testing sets. 80% of the data is used for training and 20% for testing. The testing data is kept separate to evaluate the model on unseen data.
</p>

<h3>11. Feature Selection</h3>
<p>
The most useful features are selected using <code>SelectKBest</code>. Feature selection is performed after splitting the data to prevent information from the testing dataset from influencing the training process.
</p>

<h3>12. Normalization</h3>
<p>
<code>StandardScaler</code> is used to scale the selected features. The scaler is fitted using the training data and then applied to the testing data to maintain consistency and avoid data leakage.
</p>

<h3>13. Logistic Regression and Model Training</h3>
<p>
A Logistic Regression model is created and trained using the selected and scaled training data. The model learns to classify each title as either a Movie or a TV Show.
</p>

<h3>14. Testing of the Model</h3>
<p>
The trained model is used on the testing data to generate predictions. The model also provides prediction probabilities for further evaluation.
</p>

<h3>15. Performance Metrics Evaluation</h3>
<p>
The model is evaluated using various performance metrics:
</p>
<ul>
    <li>Accuracy</li>
    <li>Precision</li>
    <li>Recall</li>
    <li>F1 Score</li>
    <li>Root Mean Square Error (RMSE)</li>
    <li>ROC-AUC Score</li>
</ul>
<p>
These metrics help assess how effectively the model performs its classification task.
</p>

<h3>16. Confusion Matrix Creation</h3>
<p>
A confusion matrix is created to compare actual values with predicted values. It shows the correct and incorrect classifications for Movies and TV Shows.
</p>

<h3>17. Data Visualization and Model Plots</h3>
<p>
Different graphs are created to understand the dataset and model performance. These include:
</p>
<ul>
    <li>Movies vs TV Shows distribution</li>
    <li>Release year distribution</li>
    <li>Most common genres</li>
    <li>Logistic Regression coefficients</li>
    <li>ROC Curve</li>
</ul>

<h3>18. Movie Recommendation</h3>
<p>
The recommendation system considers only movies and compares their genres. A similarity score is calculated between the selected movie and other movies to identify titles with similar genre combinations.
</p>

<h3>19. Testing the Recommendation System</h3>
<p>
The user provides a movie name, and the system searches for movies with similar genres. The movies are sorted according to their similarity scores, and the most similar movies are displayed as recommendations.
</p>

<hr>

<h2 align="center">❤️ Hope You Liked Our Project! ❤️</h2>

<p align="center">
Thank you for visiting our project repository!
  



