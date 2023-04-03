# Base image
FROM node:17.0-alpine3.14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json files
COPY package*.json ./

# Install npm package manager
RUN apk add --no-cache npm=7.17.0-r0 && npm install

# Copy app.js file
COPY app.js .

# Copy views directory
COPY index.pug favicon.ico /app/views/

# Expose port 80
EXPOSE 80

# Start the app
CMD [ "node", "app.js" ]
