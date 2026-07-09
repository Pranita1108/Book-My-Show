# Use Node.js 18
FROM node:18

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install --legacy-peer-deps

# Copy the entire project
COPY . .

# Build the React app
RUN npm run build

# Install 'serve' to serve static files
RUN npm install -g serve

# Expose port 3000
EXPOSE 3000

# Run the production build
CMD ["serve", "-s", "build", "-l", "3000"]
