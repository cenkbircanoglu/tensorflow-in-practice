
```.textmate
Q1: What is a windowed dataset?
A1: The time series aligned to a fixed shape

Q2: What does ‘drop_remainder=true’ do?
A2: It ensures that all rows in the data window are the same length by cropping data

Q3: What’s the correct line of code to split an n column window into n-1 columns for features and 1 column for a label
A3: dataset = dataset.map(lambda window: (window[:-1], window[-1:]))

Q4: What does MSE stand for?
A4: Mean Squared error

Q5: What does MAE stand for?
A5: Mean Absolute Error

Q6: If time values are in time[], series values are in series[] and we want to split the series into training and validation at time 1000, what is the correct code?
A6: 
time_train = time[:split_time]
x_train = series[:split_time]
time_valid = time[split_time:]
x_valid = series[split_time:]

Q7: If you want to inspect the learned parameters in a layer after training, what’s a good technique to use?
A7: Assign a variable to the layer and add it to the model using that variable. Inspect its properties after training

Q8: How do you set the learning rate of the SGD optimizer? 
A8: Use the lr property

Q9: If you want to amend the learning rate of the optimizer on the fly, after each epoch, what do you do?
A9: Use a LearningRateScheduler object in the callbacks namespace and assign that to the callback
```