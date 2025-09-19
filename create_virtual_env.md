

### How to activate Virtual env in Jupyter notebook


1)	apt update & apt upgrade
2)	Follow instructions https://www.anaconda.com/docs/getting-started/miniconda/install#linux-terminal-installer

Or run command in terminal  directly “ wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh ”

3)	bash Miniconda3-latest-Linux-x86_64.sh
4)	export PATH="$HOME/miniconda3/bin:$PATH"
5)	source ~/.bashrc

6)	check conda is installed properly or not  

      a) conda –version

      b) conda list 
If no output , it mean conda is not installed.

7 ) create virtual env 

conda create -n your_env_name python= your_Req_version 
**Example**: conda create -n sahil python=3.10

8)	conda init 
9)	conda activate your_env_name
**Example** “conda activate sahil”
  if not then close the current terminal then activate env in new terminal 

It should look like “(sahil) root@machine_name:/# ”

**install jupyter-kernel and launch**

10)	 conda install ipykernel
11)	python -m ipykernel install --user --name=the_kernel_name --display-name "the_name_That_Display_on_notebook_kernel" 	

**Example** “python -m ipykernel install --user --name=sahil --display-name "Python (sahil)"”
Select the install kernel to run jupyter file in env 
 <img width="940" height="498" alt="image" src="https://github.com/user-attachments/assets/35f5e48c-ff2e-4058-b037-f26ad7ca8fe1" />



Install req libraries by “conda install lib_name”






