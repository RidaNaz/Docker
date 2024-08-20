# Docker containerization of FastAPI application 

## 1. Create FastAPI Project

- Run this command:

```bash
poetry new <projectname>
```

- navigate to the directory:

```bash
cd <projectname>
```

- Run this command to install dependencies:

```bash
poetry add fastapi uvicorn
```

## 2. Create `main.py` File

- Create `main.py` file in the navigated project file and paste this boiler plate code in this file:

```py
from fastapi import FastAPI

aap = FastAPI()

@app.get("/")
async def root():
    return {"message" : "Hello World"}
```

## 3. Run the FastAPI Application

- Run this command where the `pyproject.toml` is located (main terminal of project):

```bash
poetry run uvicorn <projectname>.main:app --reload
```

- Open this URL in browser:

![Ss](/05_fastapi-containerization/public/fastapi-container.jpg)

## 4. Create Dockerfile

- Create a `Dockerfile` in the root of the project and write some commands.

- [visit Dockerfile](/05_fastapi-containerization/Dockerfile)

## 5. Run Docker Engine

- Open Docker Dekstop, it will automatically run the docker engine.

## 6. Build Image of Project

- Run this command in the terminal where the Dockerfile is located:

```bash
docker build -t <image-name> .
```

- After running this command, open ***Docker Dekstop***, navigate to the `Images`and then you can see your image here:

![Ss](/05_fastapi-containerization/public/docker-image2.jpg)

- You can also see your image from CLI by running this command:

```bash
docker image ls
```

## 7. Run and Create Container from CLI

- Run this command to see the list of docker Images:

```bash
docker image ls
```

- Then copy the Image ID and run this command with this ID:

```bash
docker run -d -p 8000:8000 --name <container-name> <image-id>
```

- After running this you get some ID, now this means your container have run.

![Ss](/05_fastapi-containerization/public/container-cli2.jpg)

- Run this command to see the list of Running Containers:

```bash
docker ps
```

![Ss](/05_fastapi-containerization/public/container-cli3.jpg)

## 8. Run and Create Container from Docker Dekstop

- Open Docker Dekstop and navigate to the Images section from left bar.
- Then click on play button to run the container.

![Ss](/05_fastapi-containerization/public/fast-container.jpg)

- After clicking, you get this window:

![Ss](/05_fastapi-containerization/public/fast-container4.jpg)

- Give name to the container and you can also change the ***Host port*** from there:

![Ss](/05_fastapi-containerization/public/fast-container2.jpg)

- After clicking on `Run`, the container will run:

![Ss](/05_fastapi-containerization/public/fast-container3.jpg)

## 9. Run Application in Browser

- You can run browser to these ports:

```bash
http://localhost:8000/

http://localhost:8001/
```