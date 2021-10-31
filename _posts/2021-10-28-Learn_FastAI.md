# Learn FastAI using Free Notebooks with GPU support

At the time of writing, Kaggle provide much better experience than the other alternatives

1. Gradient  
The free version is slow and unstable, default CPU instance live time is 1h.

2. Colab  
Can not finish run of `text_classifier_learner` due to slow GPU and get disconnected often.
Do not support running in background
Need to authorize access to drive every time

3. Kaggle  
30h free GPU run time
support running in background


Use below if encountering dependencies resolving issue during pip install

```python
!python -m pip install --upgrade pip
!pip install -Uqq fastbook --use-feature=2020-resolver
```
