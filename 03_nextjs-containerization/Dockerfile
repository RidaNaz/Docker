# To install nodejs in container by pulling or fetching the image of node-20
FROM node:20


# To make the folder naming `code` in container
WORKDIR /code


# COPY source dest    (source = from where to copy,  dest = where to paste)
# `.` :  copy all files from where the Dockerfile is
# `/code/` :  paste in the code folder that have created above
COPY . /code/


# To install all dependencies that are mentioned in `package.json` in the container
RUN npm install


# To define the port where we want to run our nextjs application
EXPOSE 3000


# To give command that runs the application (command should be in array of strings)
CMD ["npm", "run", "dev"]