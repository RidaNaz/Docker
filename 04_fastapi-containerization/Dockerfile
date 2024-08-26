# To install python image in the linux system of the container
FROM python:3.12


# To install poetry
RUN pip install poetry


# To make work directory or folder
WORKDIR /work


# To copy files from current destination (`.`)  and paste in the work directory that is created above
COPY . /work/


# To stop poetry from creating their virtual environment because container already have
RUN poetry config virtualenvs.create false


# To install the dependencies that are mentioned in `pyproject.toml` in the container
RUN poetry install


# To define the port where we want to run our fastapi application
EXPOSE 8000


# To give command that runs the application (command should be in array of strings)
CMD ["poetry", "run", "uvicorn", "fastapi-project.main:app", "--host", "0.0.0.0", "--reload"]