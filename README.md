## Problem Statement : Marketing Analytics

[ML - Developer Coding Problem 2017.pdf](https://github.com/Saurav0074/Fragma-Coding-Assessment/blob/master/ML%20-%20Developer%20Coding%20Problem%202017.pdf) contains the original description of the problem that was assigned to me while applying for the **Selection towards Developer Position - 2017** at [Fragma Data Systems](https://fragmadata.com/).
### Note: I was, however, ineligible for the job position because of the requirement of joining immediately _( Still in my senior year :-( )_.

[marketing-data.csv](https://github.com/Saurav0074/Fragma-Coding-Assessment/blob/master/marketing-data.csv) contains the data set of direct marketing campaigns of a banking institution. [main.py](https://github.com/Saurav0074/Fragma-Coding-Assessment/blob/master/main.py) contains the complete code.

### Data Exploration
- Looking at the values of the columns, the first task needed to be carried was to convert the columns with
non-numeric/string values into numeric ones. I used sklearn’s `LabelEncoder()` function for this. Below is an overview of the labelling function used:

```
# function to encode non-numeric values into set of numeric labels
def encoding_columns(X):
	encoder = LabelEncoder()
	encoder.fit(X)
	X = encoder.transform(X) # transform X based on distinct labels found
	#print(format(Counter(X))) # print count of each label
	return X

```
