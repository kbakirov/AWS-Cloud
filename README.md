# Launching Jupyter and Virtual Environment on AWS
 Launching Jupyter Notebook and Virtual Environment on AWS

## **1 Step**
 Launching EC2 instance on Ubuntu 18.04 and connecting through ssh with port **8888**.

## **2 Step**
 Checking for installed python
```
python3 --version
```
 Update
```
sudo apt-get install -y
```
install pip (same version as python pip3)
```
sudo apt-get install python3-pip -y
```
Check pip3 version
```
pip3 --version
```
## **3 Step**
Install Jupyter
```
sudo pip3 install jupyter
```
Launch Jupyter notebook
```
jupyter notebook --ip=0.0.0.0
```
Check running Jupyter notebooks
```
jupyter notebook list
```
Stop running Jupyter notebook
```
jupyter notebook stop 8888
```
Run with **nohup** (stay alive even if terminal shut down)
```
nohup jupyter notebook --ip=0.0.0.0 &
```
Get the token
```
cat nohup.out
```
## **4 Step**
Install mini-conda
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
sh Miniconda3-latest-Linux-x86_64.sh
```
Create virtual environment with python 3.6
```
conda create -n <venv_name> python=3.6
```
activate virtual environment
```
conda activate <venv_name>
```
Deactivate virtual environment
```
conda deactivate
```
List existing environments
```
conda env list  
```
Remove virtual environment (deactivate first)
```
conda env remove --name <venv_name>
```
## **5 Step**
In your virtual environment, Install in ipykernel
```
conda install ipykernel
or
pip install ipykernel
NOT --> pip3 install ipykernel !! (check warning below)
```
