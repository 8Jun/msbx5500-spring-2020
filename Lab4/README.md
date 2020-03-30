# Simple Machine Learning model deployment using Flask and Heroku

## Objective
* Understand how to use both Flask and Heroku inorder to deploy a useable machine learning model.

## Code Preview

``` python
from sklearn.datasets import fetch_openml
X, y = fetch_openml(data_id='1113', return_X_y=True, as_frame=True)
print('n records: {}'.format(len(X.index)))
X_preserved = X.copy()
y_preserved = y.copy()

def get_attack_type_downsampled_balanced_subset(attack_names, label, X, y):
    print('Attack group name: {}'.format(label))
    print('Attack_types: {}'.format(', '.join(attack_names)))
 
 ```
 
 ``` pytyhon
 #https://flask.palletsprojects.com/en/1.1.x/quickstart/#the-request-object
@app.route('/predict', methods=['GET','POST'])
def predict():
    error = None
    y_pred = None
    if request.method == 'POST':
        predict_me = {feature_name: None for feature_name in original_dataset_features}
```
