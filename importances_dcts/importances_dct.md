This is a brief description of how to use the importance_dct files and what they are.

Each of the three files is a pickle file containing a dictionary. The keys in these dicitonaries are columns of our dataframe, and the values are the feature importances. Each of these dictionaries contains the info for either the lower, middle, or upper class identified in clustering, and is denoted by the name of the file.

To load the file as a dictionary that you can interact with, use syntax like this.

import pickle  
with open(filename, 'rb') as file:  
my_dct = pickle.load(file)  
  
I can't figure out how to put a tab in a markdown file, but I'm assuming you know to use the indent after the colon.  
  
Feel free to look around the dictionaries to compare the importance of different features in each cluster.