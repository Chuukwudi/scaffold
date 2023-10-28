[![Python application test with Github Actions](https://github.com/Chuukwudi/scaffold/actions/workflows/main.yml/badge.svg)](https://github.com/Chuukwudi/scaffold/actions/workflows/main.yml)

# scaffold
This is a project scaffold for python

This project teaches Continous Integration in the cloud. You start by creating the files listed inside this project. Preferably use the 
AWS Linux instance because it intetgrates excellently with all AWS services. The advantage of this is that there is no need to save credentials and all. You work inside the cloud and do your deployments there.



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
