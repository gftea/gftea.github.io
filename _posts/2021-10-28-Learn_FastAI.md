# Alternatives of free Notebooks with GPU service


1. Gradient  
Max live time of a started instance is 6h, then will be shut down automatically.  
The GPU speed and CUDA memory is lower than Kaggle's. I hit the "CUDA out of memory error" when running the `text_classifier_learner`.  
Gradient preserve the server environment, so that the installed packages will still be available in next startup.

2. Colab  
I got much slower GPU than Gradien, I also cannot finish running of `text_classifier_learner` due to being disconnected often.  
Do not support running notebooks in background. Do not support jupyter notebook default keyboard shortcut.
Need to authorize access to drive every time the kernel reconnected/restarted.  

3. Kaggle  
Give minimum 30 hours of free GPU run time per week.  
support running the notebook in background by "save & commit".
Cannot perserve environment. Cannot import the whole github repo.


Problems I have met and their solutions
--

1. Dependencies resolving error during pip install.  
Solved by running below codes.  
```python
!python -m pip install --upgrade pip
!pip install -Uqq fastbook --use-feature=2020-resolver
```

2. Error: `RuntimeError: solve: MAGMA library not found in compilation. Please rebuild with MAGMA`.  
Solved by downgrade the pytorch version below. See details in https://www.kaggle.com/product-feedback/279990.  
```python
!pip install --user torch==1.9.0 torchvision==0.10.0 torchaudio==0.9.0 torchtext==0.10.0
```
Another way seems to fix this issue also.
```python
!conda install -c pytorch magma-cuda110 -y
```
