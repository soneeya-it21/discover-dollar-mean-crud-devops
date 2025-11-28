# --- Stage 1: Build Node Backend ---
FROM node:18-alpine

WORKDIR /app

# Copy package files
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the backend code
COPY . .

# Expose backend port
EXPOSE 8080

# Start server
CMD ["node", "server.js"]
