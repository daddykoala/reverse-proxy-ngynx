# Base image
FROM node:18-alpine AS deps

WORKDIR /app

COPY package*.json ./

ADD . /app
RUN npm install


RUN npm run build

# Expose port
EXPOSE 3000

# Start Next.js app
CMD [ "npm", "start" ]
