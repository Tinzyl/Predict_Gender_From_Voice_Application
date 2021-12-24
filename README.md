# Predict_Gender_From_Voice_Model
### This model predicts the gender given a voice. This is a classification problem, hence the SVC and the RandomForestClassifier models were used. The metric that was used to determine the performance of the models was the accuracy. The dataset was obtained from [Kaggle]('https://www.kaggle.com/primaryobjects/voicegender?select=voice.csv'). The features of the dataset are the following:
- meanfreq: mean frequency (in kHz)
- sd: standard deviation of frequency
- median: median frequency (in kHz)
- Q25: first quantile (in kHz)
- Q75: third quantile (in kHz)
- IQR: interquantile range (in kHz)
- skew: skewness (see note in specprop description)
- kurt: kurtosis (see note in specprop description)
- sp.ent: spectral entropy
- sfm: spectral flatness
- mode: mode frequency
- centroid: frequency centroid (see specprop)
- peakf: peak frequency (frequency with highest energy)
- meanfun: average of fundamental frequency measured across acoustic signal
- minfun: minimum fundamental frequency measured across acoustic signal
- maxfun: maximum fundamental frequency measured across acoustic signal
- meandom: average of dominant frequency measured across acoustic signal
- mindom: minimum of dominant frequency measured across acoustic signal
- maxdom: maximum of dominant frequency measured across acoustic signal
- dfrange: range of dominant frequency measured across acoustic signal
- modindx: modulation index. Calculated as the accumulated absolute difference between adjacent measurements of fundamental frequencies divided by the frequency range
- label: male or female

The steps which were taken to build the model were as follows:
- EDA techniques were performed, i.e.:
  - Check for any null values
  - Check the description of the dataframe
  - Figuring out the correlation among columns
  - Check for class imbalance
  - Plot the histograms
  - Drop any unnecessary columns
- Split the data into 80% training data and 20% test data
- Fit the training data to the model
- Test the model's accuracy on the test set

## Results
### Support Vector Machine
| Accuracy on Training Data | Accuracy on Test Data
| ------------------------- | ---------------------
| 95%                       | 95%

### Random Forest Classifier
| Accuracy on Training Data | Accuracy on Test Data
| ------------------------- | ---------------------
| 100%                       | 98%

The Random Forest Classifier was the best model when it came to testing on the Test Data. Since the difference between the Accuracy on the Training Data and the Accuracy on the Test Data was not big, it means the model did not overfit.

