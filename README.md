# Titanic Survivability
## Background
This project leverages the data that can be found on Kaggle's Titanic dataset which can be found in the link below. The overall goal of this model is to correctly predict if a passenger, given there class, gender, age, and other factors listed in the data dictionary, would survive the sinking.

This model serves to illustrate the impact of the evacuation protocal of the sinking of the Titanic, and how it can be improved. Along with the impact of the shortage of lifeboats.

## Metrics
### Metric Inputs
Given that this is a classification model, the first step to take is what constitutes a possitive, and negative class in the binary binary classification matrix.

- Model Classes:
  - Possitive Class: The passenger does survive
  - Negative Class: The passenger does NOT survive

With these definitions, a matrix can be used to fully illustrate how the model can acurately, and in accurately make predicitions.


![alt text](https://github.com/TheLeveyBreaks/Foundations-of-Machine-Learning/blob/main/Matrix.JPG)

## Accuracy
### Description
In any emergancy situation, protocal is taken because it proved without a doubt, that it ensures the survivability. During the night of the sinking, where 67.5% of people perished, we are exploring the protocal off "Women and children are first", given the dire circumstances created with the ship's architects.

### Calculation
'''python
acc = (TP+TN) / (TP + TN + FP + FN)
'''

This model serves to correctly predict the survivability of passengers with the protocall implimented. With that said, attention will be paid to the False Positive rate, and False Negative. A description of the False Positive Rate along with the False Negative is given below.

- False Positive Rate
'''python
# False Positive Rate
fpr = FP / (FP + TN)
'''
- 
'''python
# False Negative Rate
fnr = FN / (FP + TN)
'''

### Estimated Financial Impacts
The Titanic distaster happened in 1912. In July of 1915, a settle ment totaling of $664,000 was paid among those survived. Adjusted for today's inflation, that is $20,166,271.68. Divided up among the survivors, which totals to $28,564.12.

It is difficult to place a financial number, specifically for the Titanic due to the overall different economic circumstances during the 1910's. With that being said, to better understand the financial impacts. This project will be using the Costa Concorida sinking as reference.
Most of compensation was settled privatly. One settlement was $105,000 due to seeking compensation for PTSD and other long-term conditions. For survivors, this number will be used for compensation. 

For family members of the deceased, on average 1.1 Million was paid. 

With that being said, the Estimated Financial Impacts can be found below:


|Quadrant|Cost|
|--------|----|
|True Positive|+$105,000|
|False Positive|+$1.1 Million|
|True Negative|+$1.1 Million|
|False Negative|+$105,000|

From the research above, the company is loosing money either way when a cruse ship sinks. Regardless, there will be legal, and compensation cost. With that said, the best case scenario is having all passengers survive the ship, lowering compensation cost. 

A description for the False Positive and False Negative rate have been given above. For further clarification for the reader, below are simple definitions that are being used in this project.

- True Positive: A passenger who survived.
  - This would be the best-case scenario for all groups involved. Indeed there is a cost associated, however ensuring the survivability will leave less financial and legal headache to deal with the distaster.
- False Postiive: A passenger who was expected to survive, but does not.
  - As described above, is the worst case scenario (given that this results in a loss of life). Even if the loss of life cannot be quantified, given the settlements of the Costa Concordia, the $1.1Million will be used. 
- True Negative: A passenger who perrished.
  - This is reflective of a passenger who is expected to perish. Of course, this outcome is not desired by anyone. However, in this case, the model is looking at the effectiveness of the "Women and Children First" for the evacuation protocol. With that said, the True Negative can serve as the bottom line cost of this protocal.
- False Negative: A passenger who was expected to perish, but survived.
  - Indeed this is a desired outcome as this results in the survival of a passenger. Again, this metric will be closely looked at as the False Negative encompasses parties that were outside the "Women and Children First" protocol. 








