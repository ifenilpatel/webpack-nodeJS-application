# webpack-nodejs-application

A simple Node.js application using Webpack for bundling.

## Overview

This project demonstrates a basic Node.js server with Webpack configurations for both development and production environments.

## Key Files

- **`server.js`**: The main server file using Express. It listens on port 3000 and serves "Hello World!" at the root URL.

- **`webpack.dev.js`**: Webpack configuration for development mode.

  - **Purpose**: Bundles the application for development with source maps enabled.
  - **Output**: `dist/dev/server.bundle.js`
  - **Mode**: Development
  - **Features**: Uses `babel-loader` for JavaScript transpiling, and `webpack-node-externals` to exclude Node.js modules from the bundle.

- **`webpack.prod.js`**: Webpack configuration for production mode.
  - **Purpose**: Bundles the application for production.
  - **Output**: `dist/prod/server.bundle.js`
  - **Mode**: Production
  - **Features**: Similar to development but optimized for production without source maps.

## Dependencies

- **`express`**: Framework for building the server.
- **`@babel/core`, `@babel/preset-env`, `babel-loader`**: For transpiling JavaScript.
- **`webpack`, `webpack-cli`, `webpack-node-externals`**: For bundling the application.
- **`cross-env`**: To set environment variables.
- **`rimraf`**: To clean directories before building.

## Scripts

- **Build Development**: `npm run build:dev`
- **Build Production**: `npm run build:prod`
- **Start Development Server**: `npm run start:dev`
- **Start Production Server**: `npm run start:prod`
