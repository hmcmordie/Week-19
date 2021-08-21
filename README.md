# Week 19 Challenge

# Purpose
The purpose of this project was to create a machine learning model that would help advise our client on which charities to donate their money to. We took an input dataset of features and a target of if the donation was successfull, and used this to create our model in which we picked the most likely charities to be our donation recipient.

# Preprocessing

- Our target is the IS_SUCCESSFUL column
- Our Features are everything except IS_SUCESSFUL, EIN, and NAME
- The Feautres that should be removed are the identifiers EIN and NAME

# Compiling, Training, and Evaluating
- I ended up with 100 Neurons per layer, 3 layers, and Relu and Sigmoid functions. I chose the neurons because I was desperate to increase accuracy so I tried increasing neurons, which seemed to help minimally. I also added a third layer to see if mixing activations would have an effect on accuracy, I noticed a third layer added minimal benefits, a fourth did not help, so it was removed. I tried a variety of things to increase accuracy, I increased and decreased neurons, I added extra hidden layers, I increased epochs, I tried every combination of activations that I could think of, I changed the binning size for the classification and application type columns, I removed every combination of columns, and finally I tried different optimizers other than Adam. None of this had anything more than marginal benefits. 

# Summary
The model was moderately accurate, 73% certainly beats a coin toss for recommendations for donation recipients, but it has room for improvement before I would want to implement it for a company. A random forest model would also be able to tackle this problem. I think the multiple weak learner algorithms would do well with the number of different features we have in this data set. I think it would do a good job sorting through some of the noise and extra data to help create an accurate result. 