
# Step 1: Use the official Node.js image
FROM node:18

# Step 2: Set working directory inside the container
WORKDIR /usr/src/app

# Step 3: Copy package.json and package-lock.json
COPY package*.json ./

# Step 4: Install dependencies
RUN npm install

# Step 5: Copy the rest of the app's source code
COPY . .

# Step 6: Build the React app for production
RUN npm run build

# Step 7: Install a lightweight HTTP server to serve the static files
RUN npm install -g serve

# Step 8: Expose the port the app runs on
EXPOSE 3000

# Step 9: Command to serve the app
CMD ["serve", "-s", "build"]