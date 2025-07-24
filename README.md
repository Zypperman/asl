# asl

Project Polish - ASL

forked from <https://github.com/auyeongweibin/asl>.

## Deploying from the ground up (on Windows)

1. Install Git, Visual Studio Code and Node.Js Package Manager (NPM) on your machine.

2. Click the `<Code>` button on the repository page, then click "HTTPS" and copy the provided link.

3. Decide on an easily accessible folder on your machine (ie your desktop), open it with your terminal and download the repository into it with `git clone <repository_link>`.

4. Access powershell from the integrated terminal in vs code (the default shortcut for doing this is `` CTRL + ` `` ) and create a python virtual environment (we'll name it `ASL_venv`):

    ```powershell
    ".\PythonInstallation(3.9.13)\python.exe" -m venv ASL_venv  
    ```

5. Activate the python virtual environment, `ASL_venv`, from the terminal

    ```bash
    .\ASL_venv\Scripts\activate
    ```

    You'll know its running if your terminal has `(ASL_venv) PS <foldername>` appended to your command line, it'll look like:

    ```bash
    (ASL_venv) PS C:\Users\Username\Desktop\asl>
    ```

6. Install the packages and prerequsite scripts for the server (they should already be installed, so run this script just to make sure)

    ```bash
    pip install -r requirements.txt && npm i
    ```

7. Start the flask server

    ```bash
    flask run
    ```

    You'll eventually see the line:

    ```bash
     * Running on http://127.0.0.1:5000
    ```

    visit <http://localhost:5000/> to view the project.

## Fixes

Due to a breaking change made in pytorch 2.6, you need to explicitly change the `torch.load` function's `weights_only` attribute to `False` in the Ultralytics package. This has been done in the provided virtual environment.

## Issues

This project can be built into a Docker Container successfully, but the virtual machine running it needs to be able to access the filepath to your camera.
