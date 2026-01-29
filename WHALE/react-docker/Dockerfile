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




