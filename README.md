# auntoencoder-copd-demo
A basic version of the containerized Autoencoder Code built on JupyterHub's tensorflow notebook. 
Other required packages have been added through the requirements.txt file. 
It also allows the user ($NB_USER) to install libraries and packages using Conda.

To start the standalone notebook, use ```docker run -i <container-name>``` or, ```docker run -i heliumdatastage/autoencoder-demo:<tagname>``` 
This will give you the authentication token to log into the jupyternotebook running at http://localhost:8888.

Alternatively to get the authentication token, 
use the command ```docker run -d -p 8888:8888 <container-name>``` 
(for example, ```docker run -d -p 8888:8888 heliumdatastage/autoencoder-demo:<tagname>```) followed by ```docker ps -a``` to get the container- ID. 
Once you have the container ID, you will be able to access the authentication token by running 
```docker exec -t -i <container-id> /bin/bash``` which will launch the notebook shell. 
Once inside the notebook shell, type jupyter notebook list to get the token.

Use this token to log in to your jupyter notebook running at http://localhost:8888. 
You will find the machine learning code in the Autoencoder_DL folder. 
To test, run the 1st cell in COPDG_random.ipynb.
