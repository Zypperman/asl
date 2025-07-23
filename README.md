# BIA 2023 ASL Demo

Runs with Python 3.9.13.
  
  [Forked from asl project by auyeongweibin the GOAT.](https://github.com/auyeongweibin/asl#)

## Deploying from the ground up

1. Install Git and vs code on your machine.

2. Find some easily accessible folder on your machine (ie your desktop) and download the repository with `git clone <repository_link>` (click the `<Code>` button on the repository page, then click "HTTPS" and you will get a provided link).

3. Open the project in vs code and access the terminal from within vs code
    - (the default shortcut for doing this is `` CTRL + ` ``  )

4. Activate the python virtual environment, `ASL_venv`, from the terminal

    ```bash
    .\ASL_venv\Scripts\activate
    ```

    You'll know its running if your terminal has `(ASL_venv) PS <foldername>` appended to your command line, it'll look like:

    ```bash
    (ASL_venv) PS C:\Users\Username\Desktop\asl>
    ```

5. Install the packages and prerequsite scripts for the server

    ```bash
    pip install -r requirements.txt && npm i
    ```

6. Start the flask server

    ```bash
    flask run
    ```

    You'll eventually see the line:

    ```bash
     * Running on http://127.0.0.1:5000
    ```

    visit <http://localhost:5000/> to view the project.

## Fixes

Due to a breaking change made in pytorch 2.6, you need to explicitly change the `torch.load` function's `weights_only` attribute to `False` in the Ultralytics package.

## Issues

This project can be built into a Docker Container successfully, but the virtual machine running it needs to be able to access the filepath to your camera.
