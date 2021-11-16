# Knowledge Junction  

This will show you random posts from Reddit. Made using Jinja2, FastAPI, and SQLAlchemy.

To run it locally: 

Clone the repository
```
git clone git@github.com:SpecterX-AHM/Knowledge-Junction.git
```

Create a virtual environment using Anaconda or Miniconda.
```
conda create -n kj python=3.9.7
conda activate kj
```

Install the required packages.
```
pip install -r requirements.txt
```  

Now, Go to app/utils/reddit_api.py and change SECRET_KEY, CLIENT_ID, REDDIT_USERNAME, and REDDIT_PASSWORD to your own. 
For the password, you have to create a pswd.txt inside the utils folder.  
```
python main.py
```

Go to localhost:8800 to see the application.

### Run using Docker  

Build a docker image using the Dockerfile.
```
docker build -t kj:1.1 .
```
name = name of the container  
-d = container will run in detached mode  
-p 80:8800 = bind the local port 80 to the docker port 8800  
kj:1.1 = name of the image
```
docker run --name kj -d -p 80:8800 kj:1.1
```