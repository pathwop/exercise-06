# Exercise 6

This exercise is about applying filters before classifying.

## Step 1

Please clone this repository onto your local computer. On the command line, you would enter: `git clone https://github.com/idh-cologne-tools-ressourcen-infra/exercise-06`, and create a new branch using your UzK username as a name.

## Step 2

The file `data/imdb.arff` contains a data set. The data set consists of movie reviews from IMDB, which are evaluated as positive or negative (i.e., some sentiment annotation was done). As you can see when you open the file, it contains only two columns: The review text and the sentiment evaluation.

## Step 3

Open the file in Weka. Both attributes will need to be filtered before they are of use to us.

### 3.1 Word vectors 
Each individual string in the file is unique, it is thus not very helpful for machine learning. Please convert the string attribute into a vector representation, using the filter `weka.filters.unsupervised.attribute.StringToWordVector`. Experiment with the different options. Please note that after applying this filter, a large number of new attributes will be added, such that the class attribute is no longer the last one.

### 3.2 Target class
The class attribute is represented as a numeric value. This is not usable for classification algorithms. Please convert it to a nominal data type, using an appropriate filter.


## Step 4

Train a ML model to predict sentiment scores in this data set. Depending on your filter settings (and subsequently, the number of attributes) and the classifier, each experiment might take some time (but don't wait longer than 10 minutes for a single run).

Again, post the output of the best performing classifier as a file `results.txt` in the git repository and push it to the repository.