# Restaurent-Review-System
1. import the required libraries
   
3. load the dataset
   
5. Drop the unrequired columns
   
7. Checking the null vallues in the dataset
   
9. Fill the missing values with the median
    
11. Now import the required libraries for the
    
13. This Python code appears to be preprocessing text data for natural language processing (NLP) tasks. Let's break down each step:
    
15. `import re`: This imports the regular expression (regex) module, which is used for pattern matching and manipulation of strings
    
17. `import nltk`: This imports the Natural Language Toolkit (NLTK), a popular library for NLP tasks in Python.
    
19. `from nltk.corpus import stopwords`: This imports a list of common stopwords from NLTK. Stopwords are common words in a language (e.g., "the", "is", "at") that are often removed from text data because they typically do not carry significant meaning.
    
21. `from nltk.stem.porter import PorterStemmer`: This imports the PorterStemmer class from NLTK. Stemming is the process of reducing words to their root or base form. The Porter stemming algorithm is one of the most commonly used stemming algorithms.
    
23. ps = PorterStemmer()`: This initializes a PorterStemmer object.
    
25. corpus = []`: This initializes an empty list called `corpus` where the preprocessed text data will be stored.
    
27. for i in range(0, len(X)):`: This iterates over each item in the range from 0 to the length of some variable `X`. It seems that `X` is expected to be a DataFrame or some other data structure with a column named 'Review'.
    
29. `review = re.sub('[^a-zA-Z]',' ', str(X['Review'][i]))`: This line uses the `re.sub()` function to remove any characters that are not alphabetic (i.e., non-letter characters) from the text in the 'Review' column of the `X` DataFrame. It replaces such characters with a space.
    
31. review = review.lower()`: This converts the text to lowercase. This is a common preprocessing step to ensure that the same word in different cases (e.g., "The" and "the") are treated as the same word.
    
33. review = review.split()`: This splits the text into a list of words. By default, it splits the text on whitespace.
    
35. `review = [ps.stem(word) for word in review if not word in stopwords.words('english')]`: This line uses a list comprehension to iterate over each word in the `review` list. For each word, it checks if the word is not in the list of English stopwords. If the word is not a stopword, it applies stemming using the `ps.stem()` function. The result is a list of stemmed words without stopwords.
    
36. review = ' '.join(review)`: This joins the list of words back into a single string, with each word separated by a space.
    
37. corpus.append(review)`: This appends the preprocessed review to the `corpus` list.

38. Now split the dataset into two parts: i.e. training and testing
    
40. now apply the feature selection and choose the feature which gives the most accurancy and the predictions
