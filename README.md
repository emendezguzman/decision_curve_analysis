# Decision Curve Analysis

This is the repository for the implementation of Decision Curve Analysis in Python 3. The function in this repository evaluates the clinical value of predictive models for a binary classification problem. Decision curve analysis identifies the range of threshold probabilities in which a model is of clinical value, the magnitude of benefit, and which of several models is optimal [[1]](#1).

## Instructions

### Installation

You need to have Python 3.7 [[2]](#2) or higher installed. It is recommended that you use a virtual environment:

```
sudo pip3 install -U virtualenv
virtualenv --system-site-packages -p python3 ./my_venv
source ./my_venv/bin/activate
```

Install all required Python packages using:

```
pip install -r requirements.txt
```

Clone the repository:

```
git clone https://github.com/emendezguzman/decision_curve_analysis.git
```

Finally, import our functions into your Python code using:

```
from decision_curve_analysis import *
```

## Decision Curve Analysis Functions

### DCA for Binary Classifier

This function calculates the net benefit for a scikit-learn [[3]](#3) based binary classifier (the model must have the .predic_proba method available).
Please using this function using the following syntaxis:

```
decision_curve_analysis(clf, X_test, y_test, p_min, p_max, epsilon)
```

### Net Benefit ('Treat-All Clinical Alternative')

This auxiliary funtion generates the net benefit for the 'Treat-All' clinical alternative given a set of threshold probability values.
You can call the function as follows:

```
calculate_net_benefit_all(tp_test, tn_test, p_min, p_max, epsilon)
```

### Plotting Decision Curve Analysis

Finally, this function generates the decision curves for a list of binary classifiers (scikit-learn based), including the 'Treat-None' and 'Treat-All' clinical alternatives.
Please call the function using the following command:

```
plot_decision_curves(clfs, labels, X_test, y_test, p_min, p_max, epsilon, net_benefit_lower, net_benefit_upper)
```

## References
<a id="1">[1]</a> 
Vickers, A. & Elkin, B. (2006). 
Decision curve analysis: a novel method for evaluating predicion models. 
Medical Decision Making 26, no. 6 (2006): 565-574.

<a id="2">[2]</a>
Van Rossum, Guido and Drake, Fred L. (2009).
Python 3 Reference Manual
CreateSpace.

<a id="3">[3]</a> 
Pedregosa, F., Varoquaux, G. et al. (2011)
Scikit-learn: Machine learning in Python
Journal of machine learning research, no. 12 (2011): 2825-2830.
