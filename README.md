# FSD Hosting a Full-Stack Application

Although software development is often considered the most important part of an apps life-cycle, deployment tends to be overlooked, for without deploying an app, no matter how great the app is, end users cannot use it. So far in this course we have focused on software development.

This project was involved with the deployment process. Deployment within a CI/CD environment, that is, a Continuous Integration (automatic build and testing), together with Continuous Deployment (automation of the software release process) 


# Introduction/Overview of Services/Functionality
---

Taking a Full-Stack application (Backend and Frontend) and deploying it to a cloud service provider allows the app to universally be available for end-users.

I have elected to utilise the provided 'starter' project to gain a better feel for the DevOps process and having to deal with software projects from an unknown source. 

The supplied app is a simple image sharing app called Udagram.
Users register new accounts, login and post images with captions that can be shared with other users.

In order to make the service available the following services/technologies were used:

* Amazon Web Services
    * S3 (Simple Storage Service)
    * Elastic Beanstalk (Runs and manages web apps)
    * RDS (Relational Database Services)

* CircleCi
    * Pre-built Orb integration (aws s3 & EB)
    * Github integration to trigger builds
    * Pipeline flow
    * Workflow/Job integration
        * for builds
        * for approval
        * for deployment



# Application Link
The application can be found by clicking the following link: 

[Udagram_App](http://fe-udagram-app.s3-website-us-east-1.amazonaws.com)

http://fe-udagram-app.s3-website-us-east-1.amazonaws.com


The link to the CircleCI 

https://app.circleci.com/pipelines/github/cc-ud/udagram/88/workflows/81e94c73-b582-4cff-8877-a77f52c9fa14

[![CircleCI](https://circleci.com/github/cc-ud/udagram.svg?style=svg)](https://app.circleci.com/pipelines/github/cc-ud/udagram/88/workflows/81e94c73-b582-4cff-8877-a77f52c9fa14)

# Screenshots

The required and relevant screenshots can be found in the github repository

repo->docs->screenshots

# Architetcure Diagrams/Documentation

The required Diagrams & Documents can be found in the github repository

repo->docs





## About Udacity's Full Stack Javascript Developer Nanodegree

Students who graduate from the program will be able to:  
* Build client-side experiences and applications using Angular, collecting data from users and from
backends, providing rich user interactions and organizing code and data.
* Build server-side executed code with TypeScript and integrate with 3rd party code such as
Angular’s Server Side Rendering.
* Leverage Express.js to architect and build APIs that power dynamic functionality and to generate
and supply data to web and mobile clients.
* Persist data to a database, query and retrieve data, and pass this data all the way through to
various client devices.

 [Udacity Full Stack Javascript Developer Nanodegree](https://www.udacity.com/course/full-stack-javascript-developer-nanodegree--nd0067)
