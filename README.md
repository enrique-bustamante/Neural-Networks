# Neural-Networks


## Purpose

The purpose of this project was to create a neural or deep learning network
and fit a model to predict if a charity was worth donating to or not.


## Methodology

### Pre-processing

Upon importing the data, we noticed that the majority of the attributes were
categorical, which means we will have to determine which information is useful
and how we can make it numerical. We dropped NAME and EIN as categories since
these had no impact on outcome.

Next, we looked at how many unique values each categorical attribute had. Two
stood out as having a higher number of unique values, CLASSIFICATION, which
had 71 values, and APPLICATION_TYPE, which had 17. After reviewing the density
curves for these, I decided on bucketing all that had less than 50 in the
other bucket for CLASSIFICATION. For APPLICATION_TYPE, I set the value at less
than 1600 since most of the data were of type T3.

Having bucketed those categories, we then created a list of categories to run
One Hot Encoder on. This will give us numerical values that we can work with.
Finally, we used StandardScaler() to scale all of the data so that our model
won't be skewed in any one direction.


## Analysis

The highest I was able to get the accuracy was 73.33%. There were many
iterations attemped. I added up to 15 layers, went as high as 7 times the
number of inputs on some layers, even went as high as 500 epochs. None of
these combinations yielded the target of 75% accuracy.

I ultimately chose to simplify the model and use only 3 layers. If I had to
choose a different model, I might use PCA then feed it into a random forest.
Even, after running PCA on the data, I was still not able to get a better
accuracy.
