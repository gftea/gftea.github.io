# Alternatives of free Notebooks with GPU service

At the time of writing, Kaggle provide better experience than the other alternatives for me.

1. Gradient  
The free GPU version is slower than Kaggle, max live time of a started instance is 6h. 

2. Colab  
Can not finish run of `text_classifier_learner` due to slow GPU and get disconnected often.  
Do not support running in background.  
Need to authorize access to drive every time.  

3. Kaggle  
minimum 30 hours of free GPU run time per week.  
support running the notebook in background.  


Use below if encountering dependencies resolving issue during pip install.

```python
!python -m pip install --upgrade pip
!pip install -Uqq fastbook --use-feature=2020-resolver
```
