# Mahcine_learning_project
This is the first machine learning project

Software and account Requirement.
1. [Github Account]
2. Heroku Account
3. VS Code IDE
4. GIT cli

Creating conda environmen
.....
conda create -p <env_name> python==3.7 -y(yes/no) 
conda create -p venv python==3.7 -y 
.....
(activate conda env) - conda activate venv/

# use command prompt

i) GIT commands:
------------
1. To Add files to git
.....
git add .
.....
OR
.....
git add <file_name>
.....

2. Note: To ignore file or folder from git we can write name of file/folder in 
 <.gitignore file>

3. To check the git status
.....
git status
.....

4. To check all version maintained by git
.....
git log
.....

5. To create version/commit all changes by git
.....
git commit -m "message"
.....

6. To send version/changes to github
.....
git push origin main
.....

7. To check remote url
.....
git remote -v
.....

ii) To setup CI/CD pipeline in heroku we need 3 information

HEROKU_EMAIL = sreemanbitsmech@gmail.com
HEROKU_API_KEY = e9171a6d-ccd3-44ea-a07b-45f85bf3d096
HEROKU_APP_NAME = ml-algo-app
BUILD DOCKER IMAGE

docker build -t <image_name>:<tagname> .
Note: Image name for docker must be lowercase

To list docker image

docker images
Run docker image

docker run -p 5000:5000 -e PORT=5000 f8c749e73678
To check running container in docker

docker ps
Tos stop docker conatiner

docker stop <container_id>

Dockerfile:
-----------
=> CMD gunicorn --workers=4 --bind 0.0.0.0:$PORT app:app
    app : app -> module_name : flask_object
    gunicorn -> tool to connect 
    workers -> like n_jobs
=> EXPOSE $PORT 
    $PORT -> port environment variable that we recieve from Heroku machine

=> how to run setup.py
...
python setup.py install
....
=> installing all dependensies including housing pckg
... we need setup.py file to use "-e ."
In requirements.txt  -> we can add "-e ." at the last line
In terminal:
"pip install -r requirements.txt"
...

=> Jupyter notebook
.....
pip install ipykernel
.....
