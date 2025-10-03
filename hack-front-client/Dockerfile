# Use official Node.js image
FROM node:20-alpine

# Set working directory
WORKDIR /app

# Install dependencies required for React Native Web and Metro
RUN apk add --no-cache bash git python3 make g++

# Copy package.json and package-lock.json first (for caching)
COPY package*.json ./

# Install project dependencies
RUN npm install

# Copy the rest of the app
COPY . .

# Expose Metro bundler default port
EXPOSE 19006

# Start the React Native dev server in web mode
CMD ["npm", "run", "web"]
