Deploying a Flask API
Demo URL
http://af3dd12ebb6cd11e9bea1065fe5a4733-1388989332.us-west-2.elb.amazonaws.com/

Introduction
This is the project starter repo for the fourth course in the Udacity Full Stack Nanodegree: Server Deployment, Containerization, and Testing.

In this project you will containerize and deploy a Flask API to a Kubernetes cluster using Docker, AWS EKS, CodePipeline, and CodeBuild.

The Flask app that will be used for this project consists of a simple API with three endpoints:

GET '/': This is a simple health check, which returns the response 'Healthy'.
POST '/auth': This takes a email and password as json arguments and returns a JWT based on a custom secret.
GET '/contents': This requires a valid JWT, and returns the un-encrpyted contents of that token.
The app relies on a secret set as the environment variable JWT_SECRET to produce a JWT. The built-in Flask server is adequate for local development, but not production, so you will be using the production-ready Gunicorn server when deploying the app.

Initial setup
Fork this project to your Github account.
Locally clone your forked version to begin working on the project.
Dependencies
Docker Engine
Installation instructions for all OSes can be found here.
For Mac users, if you have no previous Docker Toolbox installation, you can install Docker Desktop for Mac. If you already have a Docker Toolbox installation, please read this before installing.
AWS Account
You can create an AWS account by signing up here.
Project Steps
Completing the project involves several steps:

Write a Dockerfile for a simple Flask API
Build and test the container locally
Create an EKS cluster
Store a secret using AWS Parameter Store
Create a CodePipeline pipeline triggered by GitHub checkins
Create a CodeBuild stage which will build, test, and deploy your code
For more detail about each of these steps, see the project lesson here.