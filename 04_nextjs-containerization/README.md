# Docker containerization of Next.js application 

## 1. Create Next.js Project

```bash
npx create-next-app@latest
```

## 2. Delete & Create File

- delete `node modules` file.
- Create `Dockerfile`.

## 3. Dockerfile

- Visit [Dockerfile](/04_nextjs-containerization/Dockerfile) to see what to written.

## 4. Run Docker Engine

- Open Docker Dekstop, it will automatically run the docker engine.

## 5. Build Image of Project

- Run this command in the terminal where the Dockerfile is located:

```bash
docker build -t <image-name> .
```

- After running this command, open ***Docker Dekstop***, navigate to the `Images`and then you can see your image here:

![Ss](/04_nextjs-containerization/public/docker-image.jpg)

- You can also see your image from CLI by running this command:

```bash
docker image ls
```

## 6. Run and Create Container from CLI

- Run this command to see the list of docker Images:

```bash
docker image ls
```

- Then copy the Image ID and run this command with this ID:

```bash
docker run -d -p 3000:3000 --name <container-name> <image-id>
```

- After running this you get some ID, now this means your container have run.

![Ss](/04_nextjs-containerization/public/container-cli.jpg)

- Run this command to see the list of Running Containers:

```bash
docker ps
```

## 7. Run and Create Container from Docker Dekstop

- Open Docker Dekstop and navigate to the Images section from left bar.
- Then click on play button to run the container.

![Ss](/04_nextjs-containerization/public/container-dekstop.jpg)

- After clicking, you get this window:

![Ss](/04_nextjs-containerization/public/container-docker2.jpg)

- Give name to the container and you can also change the ***Host port*** from there:

![Ss](/04_nextjs-containerization/public/container-docker3.jpg)

- After clicking on `Run`, the container will run:

![Ss](/04_nextjs-containerization/public/container-docker4.jpg)

## 8. Run Application in Browser

- You can run browser to these ports:

```bash
http://localhost:3000/

http://localhost:3001/
```