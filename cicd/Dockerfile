FROM node:14.4.0
MAINTAINER Jaeseo Kim devjaeseo@gmail.com

# Environment
ENV NODE_ENV production

# Create app directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Installing dependencies
COPY package*.json /usr/src/app/
RUN npm install --production

# Copying source files
COPY . /usr/src/app

# Building app
RUN npm run build

# Running the app
CMD ["node", "server-register.js"]