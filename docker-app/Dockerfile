# 1. Use official Node.js base image
FROM node:18-alpine

# 2. Set working directory inside container
WORKDIR /app

# 3. Copy package.json and package-lock.json first (for caching layers)
COPY package*.json ./

# 4. Install dependencies
RUN npm install --production

# 5. Copy the rest of the source code
COPY . .

# 6. Expose port (same as app PORT)
EXPOSE 3000

# 7. Command to run the app
CMD ["node", "index.js"]
