# True Positive Rate (TPR)
$$TPR = \frac{TP}{TP + FN}$$
* % True Positives based on Data Perspective

# Support (Predictive Positive Rate)
$$sup = \frac{TP + FP}{N}$$


# Precision
$$P = \frac{\textrm{True Positives}}{\textrm{True Positives + False Positives}}$$
* Performance from Model Perspective:

# Recall
$$R = \frac{\textrm{True Positives}}{\textrm{True Positives + False Negatives}}$$
* Performance from Data Perspectives
 

# F1 Score
$$F1 = \frac{2PR}{P+R}$$
* Harmonic mean of precision and recall

## ROC-AUC
* AUC stands for "area under the ROC Curve". 
* It measures the entire two dimensional area undenearth the entire ROC curve and the values ranges from 0 to 1. 
* ROC measures probability of detection (TPR) against the probability of false alarm (FPR) and created by plotting TPR along y-axis and FPR along X axis. 
* An ideal model will have 100% TPR and 0% FPR. Hence, the ideal model will move towards upper left corner of the graph. \* A random model will be represented by a diago

## Precision-Recall Curve


**Advantages of AUC **
[Reference](https://towardsdatascience.com/an-understandable-guide-to-roc-curves-and-auc-and-why-and-when-to-use-them-92020bc4c5c1)
1. It is scale-invariant i.e changes in probability values doesn't make a difference 
2. It is classification-threshold-invariant i.e. AUC score doesn't get influenced even if we change the classification threshold.


## Lift Charts


# Calibration Plots
* X axis --> Mean Predicted Probability in a given bin
* Y Axis --> Proportion of True Outcomes

![[Pasted image 20210626101506.png]]

```
from sklearn.calibration import calibration_curve
prob_true, prob_pred = calibration_curve(y_test, probs, n_bins=5)
```

# Brier Score
$$ BS = \frac{\sum_{i=1}^{n}(\hat{y}_i-y_i)^2}{n}$$

**Reference**:
* [ROC Curve, Lift Chart and Calibration Plot](http://mrvar.fdv.uni-lj.si/pub/mz/mz3.1/vuk.pdf)
* [AUC-ROC, Gains Chart and Lift Curve explained with business implications – Georgios Sarantitis ](https://gsarantitis.wordpress.com/2020/04/29/auc-roc-gains-chart-and-lift-curve-explained-with-business-implications/)
* 