# Full Stack DevOps Lab : Complete CI/CD Pipeline with Node.js, Docker, and Kubernetes

Welcome to the Full Stack DevOps Lab! This project demonstrates how to set up a complete CI/CD pipeline for a Node.js application using Docker and Kubernetes. Follow the steps below to get started.

## Prerequisites
- Installation of Nodejs 
- Docker installed on your machine
- Kubernetes cluster (Minikube, Docker Desktop, or any cloud provider)
- Git ( Version Control System)

# Step 1: Set up Git for tracking code changes locally (Version Control)

1. System wide Git Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "    
```
2. Create a Project directory & Initialize Project
```bash
mkdir my-devops-project
cd my-devops-project
git init
```
# Step 2: Build Node.js Web Application 
1. Initialize Node.js Project
```bash
npm init -y
```
2. Update package.json file with necessary dependencies
```json
{
  "name": "my-devops-project",
  "version": "1.0.0",
  "description": "DevOps learning project with Node.js",
  "main": "app.js",
  "scripts": {
    "start": "node app.js",
    "test": "jest",
    "dev": "node app.js",
    "lint": "eslint ."
  },
  "keywords": ["devops", "nodejs", "docker"],
  "author": "Your Name",
  "license": "MIT",
  "engines": {
    "node": ">=18.0.0"
  },
  "devDependencies": {
    "jest": "^29.7.0",
    "eslint": "^8.57.0",
    "supertest": "^7.1.4"
  }
}
```
3. Create a simple Application in `app.js` 
```javascript  
const express = require('express');
const app = express();
const PORT = process.env.PORT || 3000;

app.get('/', (req, res) => {
  res.send('Hello, DevOps World!');
});
app.listen(PORT, () => {
  console.log(`Server is running on http://localhost:${PORT}`);
});
```
4. Install dependencies
```bash 
npm install --save-dev jest eslint supertest
npm install
```



   
