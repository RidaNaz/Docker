# Docker Files

- A Dockerfile is a script that contains a series of instructions on how to build a Docker image.
-  It automates the process of creating Docker images by specifying the environment setup, dependencies, and application code.
- It makes easy to move applications across different platforms and infrastructures without changes.

### How to make Docker file

- In your project directory, create a file named `Dockerfile` (no extension).
- You can also create a Dockerfile for specific environment like:
    - [Dockerfile.dev](/03_docker-files/README.md#dockerfiledev)
    - [Dockerfile.prod](/03_docker-files/README.md#dockerfileprod)
- Additionaly, you also have [.dockerignore](/03_docker-files/README.md#docker-ignore-file) file

## 1. Dockerfile.dev

- **Development Tools:** Includes tools for debugging and hot-reloading.
- **Faster Iteration:** Supports real-time code updates.
- **Consistency:** Ensures a uniform development environment.
- Visit [`Dockerfile.dev`](/03_docker-files/Dockerfile.dev) file.

## 2. Dockerfile.prod

- **Optimized:** Strips unnecessary dependencies, improving performance and security.
- **Stability:** Provides a consistent, minimal environment for production.
- **Security:** Focuses on best practices for a secure deployment.
- Visit [`Dockerfile.prod`](/03_docker-files/Dockerfile.prod) file.

## 3. Docker Ignore File

- Create a file naming `.dockerignore` in your directory.
- Mention files that docker ignore while building the image.
- Visit [`.dockerignore`](/03_docker-files/.dockerignore) file.
