# Use the official Node.js image as the base image
FROM node:20-alpine
#FROM node:20.18

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json to the container
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the project files to the container
COPY . .

# Build the Nuxt app (for production)
RUN npm run build

# Expose port 3000 for the Nuxt app
EXPOSE 3000

# Start the Nuxt server
CMD ["npm", "run", "start"]


# docker build -t nuxt-20:0.0.1 .
