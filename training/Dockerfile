# Base image
FROM node:18-alpine AS deps

# Create app directory
WORKDIR /app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available
COPY package*.json ./

RUN npm install

# Bundle app source
# Copy all other source code to work directory
ADD . /app

# Build Next.js app
RUN npm run build

# Expose port
EXPOSE 3000

# Start Next.js app
CMD [ "npm", "start" ]
