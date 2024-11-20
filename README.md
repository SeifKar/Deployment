# MERN Stack Application - Azure Deployment

This is a MERN (MongoDB, Express, React, Node.js) stack application configured for deployment on Microsoft Azure.

## Prerequisites

- Node.js and npm installed
- MongoDB Atlas account
- Microsoft Azure account
- Azure CLI installed

## Local Development

1. Install server dependencies:
   ```bash
   npm install
   ```

2. Install client dependencies:
   ```bash
   npm run client-install
   ```

3. Update the .env file with your MongoDB Atlas connection string:
   ```
   MONGODB_URI=your_mongodb_atlas_connection_string
   ```

4. Run the development server:
   ```bash
   npm run dev
   ```

## Deployment to Azure

1. Create a Web App in Azure Portal:
   - Choose Node.js as your runtime stack
   - Select your desired pricing tier

2. Configure deployment:
   - In Azure Portal, go to your Web App's Deployment Center
   - Choose your preferred deployment method (Git, GitHub, etc.)

3. Set environment variables in Azure:
   - In Azure Portal, go to your Web App's Configuration
   - Add the following application settings:
     - MONGODB_URI
     - NODE_ENV=production

4. Deploy your application:
   - If using Git, add Azure as a remote and push your changes
   - If using GitHub, connect your repository and trigger deployment

5. Your application will be available at: https://your-app-name.azurewebsites.net

## Project Structure

- `/client` - React frontend application
- `server.js` - Express backend server
- `web.config` - Azure deployment configuration
- `.env` - Environment variables (do not commit to version control)

## Scripts

- `npm start` - Start the production server
- `npm run server` - Start the development server with nodemon
- `npm run client` - Start the React development server
- `npm run dev` - Run both backend and frontend in development mode
- `npm run build` - Build the React application for production
