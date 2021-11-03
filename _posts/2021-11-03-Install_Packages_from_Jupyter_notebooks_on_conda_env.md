# Important! Below is the correct way to install package to the current Jupyter Kernel

1. Use conda 

```python
# Install a conda package in the current Jupyter kernel
import sys
!conda install --yes --prefix {sys.prefix} numpy
```

2. Use pip
```python
# Install a pip package in the current Jupyter kernel
import sys
!{sys.executable} -m pip install numpy
```

# Below is the problematic way. It install the pkg using the default executable from the shell, but not from jupyter kernel

```python
!conda install <pkg>
!pip install <pkg>
```

# Modify kernel startup
See good article about this from [jakevdp](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/#The-Root-of-the-Issue)
