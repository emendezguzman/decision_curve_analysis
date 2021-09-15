# Decision Curve Analysis

This is the repository for the implementation of Decision Curve Analysis in Python. The function in this repository evaluates the clinical value of predictive models for a binary classification problem. Decision curve analysis identifies the range of threshold probabilities in which a model is of clinical value, the magnitude of benefit, and which of several models is optimal [[1]](#1).

If you use this code in your work, then please cite our paper [link].

## Instructions

### Installation

You need to have Python 3.7 or higher installed. It is recommended that you use a virtual environment:

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

## Decision Curve Analysis


## References
<a id="1">[1]</a> 
Vickers, A. & Elkin, B. (2006). 
Decision curve analysis: a novel method for evaluating predicion models. 
Medical Decision Making 26, no. 6 (2006): 565-574.
