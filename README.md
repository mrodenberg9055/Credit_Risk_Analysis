# Credit_Risk_Analysis

##Overview of the analysis
- The purpose of this analysis was to gauge credit risk by using various different Machine Learning models.  Since credit risk is inherently an unbalanced classification problem due to the amount of good loans greatly out numbering the bad ones we will test a number of different models that oversample, undersample or a combination of the two the data for us to analyze.  

##Results of the Analysis
### Balanced Acuracy 
- The balanced accuracy scores for the oversampling and undersampling models are all roughly abou the same between .65 and .68. The lowest of the 6 different models tested was the combination approach using the SMOTEEN model, this score was well behind all of the rest.  The highest scores came from the new models, and of those too the EasyEnsembleClassifier produced a score of .93 which was .16 points higher than the other closest model.  
  - RandomOverSampler 
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampler.PNG)
  - SMOTE
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/SMOTE.PNG)
  - ClusterCentroids
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/ClusterCentroids.PNG)
  - SMOTEENN
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/SMOOTEEN.PNG)
  - BalancedRandomForestClassifier
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.PNG)
  - EasyEnsembleClassifier
- ![analysis](https://github.com/mrodenberg9055/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleClassifier.PNG)

### Precision and recall scores
- The precision scores across all the different models were very similar, little if any change between them and it was always very high.  The recall was where we saw the biggest difference from model to model.  For the RandomOverSampler, SMOTE and SMOTEEN models the avg score was between .60 and .69, moving into the ClusterCentroids model where that number drops to .40.  Looking at the other models we see a significant jump to .88 for the BalancedRandomForestClassifier and the highest number at .94 for the EasyEnsembleClassifier model.  

Summary: 
- I would make the recommendation that we use the EasyEnsembleClassifier model for the reasons that the balanced accuracy score were the highest out of any of the models we tested.  As well as it having the highest precision and recall as well.  We can assume that this model will return many results with those results being labeled correctly based on these scores.  
