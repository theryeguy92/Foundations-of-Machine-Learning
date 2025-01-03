# Titanic Survivability 
## Background
This project leverages the data that can be found on Kaggle's Titanic dataset which can be found in the link below. The overall goal of this model is to correctly predict if a passenger, given there class, gender, age, and other factors listed in the data dictionary, would survive the sinking.

This model serves to illustrate the impact of the evacuation protocal of the sinking of the Titanic, and the effect of "Women and Children First". Along with the impact of the shortage of lifeboats.

Link: https://www.kaggle.com/competitions/titanic

## Metrics
### Metric Inputs
Given that this is a classification model, the first step to take is what constitutes a possitive, and negative class in the binary classification matrix.

- Model Classes:
  - Possitive Class: The passenger does survive
  - Negative Class: The passenger does NOT survive

With these definitions, a matrix can be used to fully illustrate how the model can acurately, and inaccurately make predicitions.


![alt text](https://github.com/TheLeveyBreaks/Foundations-of-Machine-Learning/blob/main/Matrix.JPG)

- Matrix Quadrants:
  - **True Positive (TP)**: The passenger predicted to survive, does survive.
  - **True Negative (TN)**: The passenger predicted to perish, does perish.
  - **False Positive (FP)**: The passenger predicted to survive, perishes.
  - **False Negative (FN)**: The passenger predicted to perish, does NOT Perish.





## Accuracy
### Description
In any emergancy situation, protocol is taken because without a doubt, it ensures survivability. During the night of the sinking, where 67.5% of people perished, we are exploring the protocal of "Women and children are first", given the dire circumstances created with the ship's architects.

### Calculation
```
acc = (TP+TN) / (TP + TN + FP + FN)
```

This model serves to correctly predict the survivability of passengers with the protocall implimented. With that said, attention will be paid to the False Positive rate, and False Negative. A description of the False Positive Rate along with the False Negative is given below.

## False Positive Rate
This is the worst case scenario of an inacurate model, leading to loss of life regardless of the protocol implimented. This will be captured when the model creates a "false positive" for an individual. Per the definition above, this takes into effect when the model predicts an individual will survive, but does not. What makes this case so grave is that regardless of protocol, this means that there is some outside factor that the protocol did not consider, and in result, a person perishes. 

```
fpr = FP / (FP + TN)
```
## False Negative Rate
In this case, this serves as a positve for the model because this is reflective of an individual who was expected to perish, does not. More importantly, given that this dataset identifies the relationships amongst the passengers. The False Negative bucket can serve as an investigation point as to why someone who was expected to perish, survived. Taking this into consideration, indeed this is a positive element (as it lowers cost as described below), it does mean the model was not as percise in a way.

```
fnr = FN / (FP + TN)
```

### Estimated Financial Impacts
The Titanic distaster happened in 1912. In July of 1915, a settlement totaling of $664,000 was paid among those survived. Adjusted for today's inflation, that is $20,166,271.68.
Even if $20 Million is a large sum, for having a casualty rate of over 65% still seems on the lower end. Compared to the recent sinking of The Costa Concordia, where the total payout was about $91 million dollars, $20 million falls short of today's standards. Especially since today's cruise ships are bigger, and hold more capacity than the Titanic. 
With that said, this project will be using the Costa Concorida sinking as reference for the financial cost.

For the Costa Concordia, the majority of settlements were settled privatly. However, one settlement was $105,000 due to seeking compensation for PTSD and other long-term conditions. Given that these settlements were on par with eachother, seeking compensation for damages, $105,000 will be used as the total compensation for survivors. 

For family members of the deceased, $1.1 Million was paid out on average. 

With that being said, the Estimated Financial Impacts can be found below:


|Quadrant|Cost|
|--------|----|
|True Positive|+$105,000|
|False Positive|+$1.1 Million|
|True Negative|+$1.1 Million|
|False Negative|+$105,000|

From the research above, the company is loosing money either way when a cruse ship sinks. Regardless, there will be legal, and compensation cost. With that said, the best case scenario is having all passengers survive the ship, lowering compensation cost. 

A description for the False Positive and False Negative rate have been given above. For further clarification, below are simple definitions that are being used in this project.

- True Positive: A passenger who survived.
  - This would be the best-case scenario for all groups involved. Indeed there is a cost associated, however ensuring the survivability will leave less financial and legal headache to deal with the distaster.
- False Postive: A passenger who was expected to survive, but does not.
  - As described above, is the worst case scenario (given that this results in a loss of life). Even if the loss of life cannot be quantified, given the settlements of the Costa Concordia, the $1.1Million will be used. 
- True Negative: A passenger who perished.
  - This is reflective of a passenger who is expected to perish. Of course, this outcome is not desired by anyone. However, in this case, the model is looking at the effectiveness of the "Women and Children First" for the evacuation protocol. With that said, the True Negative can serve as the bottom line cost of this protocal.
- False Negative: A passenger who was expected to perish, but survived.
  - Indeed this is a desired outcome as this results in the survival of a passenger. Again, this metric will be closely looked at as the False Negative encompasses parties that were outside the "Women and Children First" protocol. 








