# Use the slim version of Node.js on Debian Bookworm as the base image
FROM node:20-bookworm-slim

# Set the working directory to /app
WORKDIR /app

# Copy package.json and package-lock.json into the container at /app
COPY package*.json ./

# Install any needed packages specified in package.json using npm ci for a clean install
RUN npm ci

# Copy the current directory contents into the container at /app
COPY . .

# Make port 3000 available to the world outside this container
EXPOSE 3000

# Run the app when the container launches
ENTRYPOINT ["node", "main.js"]
