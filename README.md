COSC Hackweek – GitHub Actions Pipeline Challenge
=================================================

Challenge:
----------
Create a GitHub Actions workflow that:

1. Sets up a Node.js environment
2. Logs the message: Hello from @Manasa-iota

Repository Contents:
--------------------
1. index.js
   - Contains a single line of code:
     console.log("Hello from @Manasa-iota");

2. .github/workflows/node-log-message.yml
   - Defines a GitHub Actions workflow that:
     • Runs on push, pull request, or manual trigger
     • Uses a matrix to test across Node.js versions 16, 18, 20, and 22
     • Installs dependencies (if any)
     • Executes the script using `npm start`

3. package.json
   - Defines the start script to run `index.js` via: node index.js

How to Run Locally:
-------------------
1. Install Node.js
2. In the project folder, run:
   npm install
   npm start

Workflow Trigger Methods:
-------------------------
- On push to `main` branch
- On pull request to `main` branch
- Manually via GitHub UI

Docker Image
============

This project is containerized using a minimal Node.js 22 Alpine image and published to Docker Hub.

Docker Hub Repository:
user1729/cbit-hackweek-github-actions-pipeline

How to Use:
-----------

1. Pull the Docker image:

   docker pull user1729/cbit-hackweek-github-actions-pipeline:v1

2. Run the container:

   docker run user1729/cbit-hackweek-github-actions-pipeline:v1

3. Expected output:

   Hello from @Manasa-iota

You can also use the latest tag:

   docker run user1729/cbit-hackweek-github-actions-pipeline:latest


Author:
-------
@Manasa-iota

Submitted for:
--------------
COSC Hackweek – Build a GitHub Actions Pipeline (DevOps | 400 Points)
