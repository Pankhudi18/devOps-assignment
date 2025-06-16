# Dockerize and Deploy a Web App on AWS EC2

## Task 1: GitHub Repository
- Repository: https://github.com/Pankhudi18/devOps-assignment.git


## Dockerizing the Application

### Dockerfile

```Dockerfile
FROM node:18
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "app.js"]

## Build and Run Locally

To test the Dockerized application on your local machine before deploying to the cloud:

### Commands

```bash
docker build -t devops-assignment-app:v1 .
docker run -p 5000:3000 devops-assignment-app:v1



