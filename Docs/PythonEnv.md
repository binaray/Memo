# Python environment quickstart

```
conda create --name py37 python=3.7
conda activate py37
conda update --all
conda install -c anaconda opencv
pip install imutils
pip install pyzmq

# for kernel switching in jupyter
conda install ipykernel
```

Reference: https://docs.openvino.ai/latest/openvino_docs_install_guides_installing_openvino_conda.html

For mac or if pip does not exist:

1. Run conda create -n venv_name and conda activate venv_name, where venv_name is the name of your virtual environment.
2. Run conda install pip. This will install pip to your venv directory.
3. Find your anaconda directory, and find the actual venv folder. It should be somewhere like /anaconda/envs/venv_name/.
4. Install new packages by doing /anaconda/envs/venv_name/bin/pip install package_name or pip install opencv-python if running from conda prompt
