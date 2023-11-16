# ML Project Process_Day 1:
---

1. Create repository in github

2. Create a folder with same name in the local drive and copy path of the folder.

3. Open anaconda prompt run command to change directory same created folder(ML Project)
   cd <path of folder>
   directory name:
   code .

4. Then VS code is open --> open terminal --> conda create -p venv python==3.11.5(current version) --> conda activate venv/

5. Now link github repo to vs code --> git init and create readme.md file

6. git commit -m "first commit" --> git status (to  check file status) --> git branch -M main -->git remote add origin https://github.com/AkashBabu1712/ML-Project.git.

7. sync git global with username and email --> git push -u origin main

8. (gitignore file) create in github

9. Create setup.py file -- responsible for build machine learning as a package and required.txt
    
   --- 
from typing import List

from setuptools import find_packages,setup

HYPEN_E_DOT='-e .'
    def get_requirements(file_path:str)->List[str]:
    
    //this function will return the list of requirements
    
    requirements=[]
    with open(file_path) as file_obj:
        requirements=file_obj.readlines()
        requirements=[req.replace("\n","") for req in requirements]

        if HYPEN_E_DOT in requirements:
            requirements.remove(HYPEN_E_DOT)
    
    return requirements


setup(
name='ML Project',

version='0.0.1',

author='Akash',

author_email='kumar111aakash.in@gmail.com',

packages=find_packages(),

install_requires=get_requirements('requirements.txt')

)
---

10. Create src folder --> (__init__.py file)


-->open terminal --> pip install -r requirments.txt --> git add . --> git status --> git commit -m "setup" --> git push -u origin main




