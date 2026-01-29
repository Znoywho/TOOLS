# 'FROM' set base image 
FROM node:20-alpine

# create a user with permission to run the app
# -S create the system user
# -G add the user to a group
# This is done to avoid running the app as a root
# If the app is run as root, any vulnerability in the app can be exploited to gain 
# access to the host system
RUN addgroup app && adduser -S -G app app

# Set the user run the app
USER app

# set working directory to /app

WORKDIR /app

# copy package.json and package-lock to the working directory
# Thi is done before copying the rest of the files to take advantage of Docker's cache
# If the package.sjon and package-lock.json files haven't changed, Docker when will use the cached dependencied
COPY package*.json ./ 

# Sometimes the ownership od the files in the working directory is changed to root
# and thus the app cannot access the files and throws an errors -> eacces: permission denied 
# to avoid this, change ownership of the files to the root user 

USER root

# change th ownership od the /app directory to app User 
# chown -R <user>:<group> <directory>
# chown command changes the user and/ or group ownership of for given file.

RUN chown -R app:app .

# change the user back to the app
USER app

# install dependencies 
RUN npm install

# copy the rest of the files to the working directory
COPY . .


EXPOSE 5173

# command to run the app
CMD npm run dev 


