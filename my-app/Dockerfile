# Start your image with a node base image
FROM node:22-alpine3.19

# The /app directory should act as the main application directory
WORKDIR /my-app

# Copy the app package and package-lock.json file
COPY package*.json ./

# Install node packages
RUN npm install

# Copy local directories to the current local directory of our docker image (/app)
COPY . .

ENV PORT=3000

EXPOSE 3000

# Start the app using serve command
CMD [ "npm", "run", "dev" ]