# asl
Project Polish - ASL

## Build
```
pip install -r requirements.txt && npm i
```

<<<<<<< Updated upstream
## Run 
```
flask run
```
=======
## Deploying from the ground up

1. Install Git, Visual Studio Code and Node.Js Package Manager (NPM) on your machine.

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

5. Install the packages and prerequsite scripts for the server (they should already be installed, so run this script just to make sure)

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

Due to a breaking change made in pytorch 2.6, you need to explicitly change the `torch.load` function's `weights_only` attribute to `False` in the Ultralytics package. This has been done in the provided virtual environment.

## Issues

This project can be built into a Docker Container successfully, but the virtual machine running it needs to be able to access the filepath to your camera.
>>>>>>> Stashed changes
