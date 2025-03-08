# movie-rating-review

The analysisscript employs several Python libraries for data analysis and visualization, including pandas, numpy, matplotlib, and seaborn. It begins by loading the dataset "fandango_score_comparison.csv" into a pandas DataFrame.    

Data Inspection

The script first explores the dataset by checking for missing values using data.isnull().sum() and examining the data types of each column with data.dtypes.  This is crucial for understanding the structure of the data and identifying any potential issues that might need to be addressed before further analysis.   

Data Exploration and Visualization

The analysis then delves into exploring the relationships between different movie review metrics.

Scatter Plots: Scatter plots are used to visualize the relationship between:
Rotten Tomatoes scores and Rotten Tomatoes User scores.    
Metacritic scores and Metacritic User scores.    
Metacritic user vote counts and IMDB user vote counts.    
Normalized Rotten Tomatoes scores (RT_norm) and normalized Rotten Tomatoes User scores (RT_user_norm).    
These scatter plots help to visually identify any correlations or patterns between these different review metrics.    

Kernel Density Estimation (KDE) Plot: A KDE plot is used to visualize the distribution of IMDB user vote counts, Metacritic user vote counts, and Fandango votes.  KDE plots provide a smooth estimate of the probability density function of a random variable.    

Comparison of Normalized Rating Scores:

 The script creates a subset of the data containing normalized ratings from different sources (Fandango Stars, Fandango Ratingvalue, RT_norm_round, RT_user_norm_round, Metacritic_norm, IMDB_norm, Metacritic_user_norm_round, and IMDB_norm_round).  A KDE plot is then used to compare the distributions of these normalized scores.  This allows for a comparison of how different platforms rate movies on a similar scale.    

Histogram: A histogram is used to visualize the distribution of Fandango Stars ratings.  This provides a clear picture of the frequency of different Fandango Star ratings.    

Boxplot: Boxplots are used to compare the distributions of Fandango Stars, normalized Rotten Tomatoes User scores, normalized Metacritic User scores, and normalized IMDB scores.  Boxplots are a standardized way of displaying the distribution of data based on a five-number summary: minimum, first quartile, median, third quartile, and maximum.    

Correlation Heatmap: A correlation heatmap is generated to visualize the correlation matrix of the data.  The correlation matrix shows the pairwise correlations between all variables in the dataset.  The heatmap uses color intensity to represent the strength of the correlations, with annotations displaying the correlation coefficients.  This allows for a quick overview of which variables are strongly correlated with each other.    

Predictive Modeling

The script also includes a section on predictive modeling, where a linear regression model is built to predict Fandango ratings using other rating metrics.

Data Preparation: The data is prepared by separating the features (independent variables) and the target variable (Fandango_Stars). The FILM column is dropped from the feature set.  The data is then split into training and testing sets using train_test_split.   

Feature Scaling: StandardScaler is used to standardize the features in both the training and testing sets. Feature scaling is important for linear regression models as it helps to ensure that all features contribute equally to the model.

Model Training and Evaluation: A LinearRegression model is trained on the training data. The model's predictions are then generated for the test data. The model's performance is evaluated using mean squared error (MSE) and R-squared (R2). The MSE measures the average squared difference between the predicted and actual values, while R2 measures the proportion of the variance in the target variable that is predictable from the features.

The script outputs the MSE and R2 values, providing an indication of the model's accuracy and goodness of fit.    


Sources and related content
