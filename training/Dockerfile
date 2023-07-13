# ./training/Dockerfile

# Base image
FROM node:alpine

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package*.json ./

RUN npm install

# Bundle app source
COPY . .

# Build Next.js app
RUN next build

# Expose port
EXPOSE 3000

# Start Next.js app
CMD [ "npm", "start" ]