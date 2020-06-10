# mushroom-classification

Classifying Edible vs. Poisonous Mushrooms

### The Problem

* With over 10,000 species of edible mushrooms in the world, how can we differentiate between which are safe for          consumption,   and which are fatal?
  
* Discerning this can be very complex, and mycologists do not possess a simple set of rules for for determining this.
  
### Data Details

* Source: UCI Repository

* The dataset contains 8123 observations of 23 species of gilled mushrooms in the Agaricus and Lepiota Families

* Each Species is classified as definitely edible, definitely poisonous, or unknown and not recommended for consumption, is grouped with poisonous.

* Observations contain 22 attributes  such as cap shape, gill size, spore-print color, etc.
 
### Model Preparation

* Created dummy variables so that all columns have numeric values(0,1)


* Dropped columns: 
  -Veil type: only contained 1 value
  -stalk root: too many values classified as “missing”


*Total of 111 features (Train / Test split (.25))

### Baseline Model

*  Random Forest Classifier

*  n estimators = 5, max depth = 5, 
  max features = auto

*  Accuracy: 0.97
*  Precision: 0.98
*  Recall: 0.97
*  F1 Score: 0.98

### Paramater Tuning

*  Grid Search Cross Validation to find optimal parameters

*  Recommended best parameters:

*  Criterion: Gini
*  Max depth: 7
*  Max features: auto
*  n estimators: 100

### Final Model

*  Random Forest Classifier

*  n estimators = 100, max depth = 7 
*  max features = auto

*  Accuracy: 1.00
*  Precision: 1.00
*  Recall: 1.00
*  F1 Score: 1.00

### Features of Importance

*  Odor! Preliminary EDA was confirmed by this Model that having no odor, or foul odor, are the biggest indicators in the observation of identifying poisonous mushrooms!

*  Gill Size “Narrow” 

*  Gill Color “Buff” (light-brown, yellowish color)

### In Conclusion

*  If the mushroom smells, has buff colored narrow gills, I’d highly advise against enjoying them in your morning omelette. 

*  Fortunately, a Random Forest Classifier can predict this with certainty. 

*  Future Work: 
   Obtain additional samples for a wider region including mushrooms of other varietals.



