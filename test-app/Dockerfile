# Use official Node.js 22 Alpine image
FROM node:22-alpine

# Install pnpm globally
RUN npm install -g pnpm

# Set working directory inside container
WORKDIR /app

# Copy package.json and pnpm-lock.yaml (if exists)
COPY package.json pnpm-lock.yaml* ./

# Install dependencies
RUN pnpm install

# Copy all project files
COPY . .

# Build the project (adjust if your build script is different)
RUN pnpm build

# Expose port 3000 for Next.js default
EXPOSE 3000

# Start the app
CMD ["pnpm", "start"]
