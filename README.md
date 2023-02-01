# Hello_world_GitHub-Action

# Follow below instruction to start your projects.

1. Create a github repo.
2. Clone github repo in your system
  ```
  git clone <github-url>
  ```
3. Open folder in vscode.

4. Create project folder structure based on standard practices.
   
   First download a bash script file.
  
  <a href="https://raw.githubusercontent.com/iNeuron-Pvt-Ltd/housing_prediciton/main/inital_bash_script.sh">
Download initial script file.
  </a>

5. Run bash script using below command

```
bash <script_name>
```
Update setup.py file with following contain
```
from setuptools import setup, find_packages

REQUIREMENT_FILE_NAME = "requirements.txt"
REMOVE_PACKAGE = "-e ."


def get_requirement_list(requirement_file_name=REQUIREMENT_FILE_NAME) -> list:
    try:
        requirement_list = None
        with open(requirement_file_name) as requirement_file:
            requirement_list = [requirement.replace("\n", "") for requirement in requirement_file]
            requirement_list.remove(REMOVE_PACKAGE)
        return requirement_list
    except Exception as e:
        raise e


setup(
    name="Housing price prediction",
    license="MIT",
    version="0.0.0",
    description="Project has been completed.",
    author="Avnish Yadav",
    packages=find_packages(),
    install_requires=get_requirement_list()
)
```

6. Add following library in requirements.txt file.

```
scikit-learn
scipy 
PyYAML
gunicorn
pandas
-e .
six
dill
Flask
```

7. Create a app.py and create a sample hello world flask app.


8. To send changes to github repo 

To add all changes into git stage
```
git add .
```

To check all files that we are about to commit.
```
git status 
```
Commit all files added in git stage
```
git commit -m "<message>"
```

If your git account is not configured.

Execute below command to configure your git.
```
git config --global user.name "<user>"
```
```
git config --global user.email "<user_email>"
```
To check remote branch url
```
git remote -v
```
To send your commit to remote branch

git push <var_name> <branch_name>



update your commited files in github repo
```
git push origin main
```

## Create an Account at heroku

Create an App at heroku
We need 3 information to setup github action
1. Heroku API KEY
2. Heroku APP Name
3. Heroku Account Emaild Id

Let's create a docker file for our application

Create file .dockerignore and Dockerfile

Create a folder directory .github/workflows/main.yaml

Check github workflow code from below link.

<a href="https://github.com/marketplace/actions/build-push-and-release-a-docker-container-to-heroku">Build and Deploy Docker image to Heroku container.</a>

Add the content from above webpage.


Add repo secret in github

Note: Kindly check your variable name in github/workflows/main.yaml file.

setting> secrets> Add new Repository Secrets.

Add folder name in .dockerignore file that are not needed in Docker image

Again send changes to Github repo.

Basic Project CI/CD setup completed.








initialize_model()


