Predicting Coronavirus Numbers with a Long-Short Term Memory Recurrent Neural Network

Challenges
1. Very small time series often <20 features in length (confirmed cases vs datetime)
2. Model with either no pre-training or being trained on other country's timeseries data

Learning points:
1. LSTMs are easy to train once they are set up properly
2. Using Facebook prophet, which is designed to predict sales patterns, was not successful here. This is 
likely due to the characteristic of that model which makes it appropriate for sales (not epidemiology)
3. Other online LSTMs may be appropriate for epidemilogical data


TODO
1. Train the LSTM on all data once it has been scaled correctly. I want to scale all the data so that it sits between -1 and 1 but
also preserve the relative differences between the number of cases. This will likely generate bizzare results as China's cases dwarf the rest
of the world's right now.
2. In light of (1) it may be appropriate to work with the number of cases on a log scale.