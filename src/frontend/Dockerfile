# Use base node 12-slim image from Docker hub
FROM node:17-slim

WORKDIR /frontend

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install --only=production

# Copy rest of the application csource code
COPY . .

# Compile the bundle
RUN npm run build

# Run the app
ENTRYPOINT ["npx", "ts-node", "app.ts"]
