[![Python application test with Github Actions](https://github.com/Chuukwudi/scaffold/actions/workflows/main.yml/badge.svg)](https://github.com/Chuukwudi/scaffold/actions/workflows/main.yml)

# scaffold
This is a project scaffold for python

This project teaches Continous Integration in the cloud. You start by creating the files listed inside this project. Preferably use the 
AWS Linux instance because it intetgrates excellently with all AWS services. The advantage of this is that there is no need to save credentials and all. You work inside the cloud and do your deployments there.



`python3 -m venv ~/.scaffold`

`source ~/.scaffold/bin/activate`

Here, you make the ability to communicate through ssh with github

`ssh-keygen -t rsa` and press `return` a few times.

`cat /home/chukwudi/.ssh/id_rsa.pub`. Here is just to print the contents of the `.pub` file which we will copy to github keys.

In sequence,
`git status` to view your file state
`git add *` to add everything un-added so you can commit them.
`git commit -m "Commit message"` to commit locally
`git push` to push to github.

NB: You must use `git pull` before attempting to edit the repo. `git pull` will update your local directory with the cloud so  you will be editing the newest version. Another altenative if you manage to mess things up will be to reclone the repo.

```

name: Python application test with Github Actions
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.8
      uses: actions/setup-python@v1
      with:
        python-version: 3.8
    - name: Install dependencies
      run: |
        make install
    - name: Lint with Pylint
      run: |
        make lint
    - name: Test with Pytest
      run: I
        make test
    - name: Format code with Python black
      run: |
        make format
        
```
