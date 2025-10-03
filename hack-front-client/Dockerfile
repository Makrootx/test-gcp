# Use Node 20
FROM node:20-alpine

WORKDIR /app

# Install system deps
RUN apk add --no-cache bash git python3 make g++

# Copy package.json first
COPY package*.json ./

# Install dependencies (including local expo)
RUN npm install

# Copy the rest of the app
COPY . .

EXPOSE 19006

# Start dev server using local Expo CLI
CMD ["npm", "run", "web"]
