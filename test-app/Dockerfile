# Use Node.js 18 base image
FROM node:22-alpine

# Set working directory
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .

# Build the app
RUN npm run build

# Expose the port Next.js runs on
EXPOSE 3000

# Run the app
CMD ["npm", "start"]
