# Jenkins Docker CI Pipeline

A small practice project demonstrating a Jenkins Declarative Pipeline with separate backend and frontend stages, each running inside a Docker container.

## Pipeline stages

- **Back-end:** Uses the `maven:3.8.1-adoptopenjdk-11` Docker image and runs `mvn --version`.
- **Front-end:** Uses the `node:16-alpine` Docker image and runs `node --version`.

## Tools used

- Jenkins
- Docker
- Maven
- Node.js
- Jenkins Declarative Pipeline syntax

## What this project demonstrates

- Defining a multi-stage Jenkins pipeline.
- Running stages in separate Docker-based environments.
- Checking tool availability and versions within each environment.

## Current scope

This is a basic pipeline exercise. It checks the installed Maven and Node.js versions only; it does **not** yet compile an application, run automated tests, build application artifacts or Docker images, or deploy an application.

## Run it

1. Use a Jenkins instance with Docker available and configured for the Jenkins agent.
2. Create a Pipeline job that loads this repository's `Jenkinsfile`.
3. Run the job and inspect the stage logs for the Maven and Node.js version output.

## Repository structure

```text
jenkins-docker-ci-pipeline/
├── Jenkinsfile
├── README.md
├── .gitignore
└── screenshots/
    └── jenkins working.png
```

The screenshot is intended to document a successful run. Review the image and confirm it accurately represents your real environment before adding it as portfolio evidence.
