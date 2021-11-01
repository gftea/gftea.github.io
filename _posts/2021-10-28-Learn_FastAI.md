# Alternatives of free Notebooks with GPU service


1. Gradient  
Max live time of a started instance is 6h, then will be shut down automatically.  
The GPU speed and CUDA memory is lower than Kaggle's. I hit the "CUDA out of memory error" when running the `text_classifier_learner`.  
Gradient preserve the server environment, so that the installed packages will still be available in next.

2. Colab  
Seems much slower GPU than Gradien, I also cannot finish running of `text_classifier_learner` due to being disconnected often.  
Do not support running notebooks in background.  
Need to authorize access to drive every time the kernel reconnected/restarted.  

3. Kaggle  
Give minimum 30 hours of free GPU run time per week.  
support running the notebook in background.  


Problems and Solutions
--

1. Dependencies resolving error during pip install.  
Solved by running below codes
```python
!python -m pip install --upgrade pip
!pip install -Uqq fastbook --use-feature=2020-resolver
```
2. Export and Import trained model.  
FastAI provide model export and import API
```python
learn.export() # export as pickled file
learn_inf = load_learner(path/'export.pkl') # import the model from the pickled file
```
