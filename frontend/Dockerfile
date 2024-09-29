FROM node:18

# Set working directory to /app
WORKDIR /usr/src/app

# Copy package*.json
COPY ./frontend/package*.json ./

# Install any needed packages
RUN npm install

# Run the command to start the development server
CMD ["npm", "start", "--", "--host", "0.0.0.0"]


