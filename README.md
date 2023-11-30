# Movie-Recommendation-System
https://colab.research.google.com/drive/1q3aaL6o5_6cHNI75xMXKxmTfJc9eoova?usp=sharing



# import pandas library 
import pandas as pd 
  
# Get the data 
column_names = ['user_id', 'item_id', 'rating', 'timestamp'] 
  
path = 'https://media.geeksforgeeks.org/wp-content/uploads/file.tsv'
  
df = pd.read_csv(path, sep='\t', names=column_names) 
  
# Check the head of the data 
df.head() 

# Check out all the movies and their respective IDs 
movie_titles = pd.read_csv('https://media.geeksforgeeks.org/wp-content/uploads/Movie_Id_Titles.csv') 
movie_titles.head()

data = pd.merge(df, movie_titles, on='item_id') 
data.head() 
