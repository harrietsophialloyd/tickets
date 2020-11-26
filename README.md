# IT Ticket Support Web Service
 
 Team 1: Alfred Joarder-White, Nickson Alemao, Atefeh Eslahi, Sam Plackett, Rajan Borkhataria, Joseph Nelson, Harriet Lloyd & Daniel Wu.


## Contents
* [Brief](#brief)
   * [Additional Requirements](#additional-requirements)
   * [Our Approach](#our-approach)
* [Architecture](#architecture)
   * [Database Structure](#database-structure)
   * [CI Pipeline](#ci-pipeline)
* [Project Tracking](#project-tracking)
* [Risk Assessment](#risk-assessment)
* [Testing](#testing)
* [Front-End Design](#front-end-design)
* [Known Issues](#known-issues)
* [Future Improvements](#future-improvements)
* [Authors](#authors)


## Brief
As a team we developed a web application based on a specification that has been provided to us, within 4 weeks. The concept is a web-hosted application that Atos employees can access to post help tickets to a publicly accessible help queue.

The application is a Spring Boot Help Queue application with full CRUD functionality for practical use as a support ticket system which will demonstrate what we have all learnt through-out our training programme. We are expected to produce a basic CI pipeline to integrate and deploy new code as it is created. 

### Additional Requirements
In addition to what has been set out in the brief, we included the following: 
* A fully functioning Help Queue web application deployed in an GCP virtual machine.
* Full documentation of the system, including project development, risk assessment, component level diagrams and installation instructions.
* A simple automated CI system, also with full documentation discussing how the tools were utilised.
* A 30 minute presentation that demonstrates:
   * our team's project management approach (team roles, sprints, product backlog, priorities, etc.)
   * the functioning application and the features that were implemented
   * the functioning CI pipeline with a fully automated rolling update   


### Our Approach
To achieve this, we produced a web-hosted ticket application that must allow Atos employees to do the following:

![usercase](images/usecasediagramv.PNG)


## Architecture
### Database Structure
This image shows our entity relationship diagram (ERD) showing the major entities within the system scope, and the inter-relationships among these entities. 

![database](images/erdv2.PNG)


### CI Pipeline

![database](images/Ci+pipeline.PNG)

The continuous integration (CI) pipeline is shows the associated frameworks and services related to them. Automated pipelines allows for rapid and simple development-to-deployment by removing manual errors and providing standardised feedback loops to developers enabling faster product iterations.
By using a local machine and pushing code to GitHub a new code will automatically pushed to Jenkins with a build trigger via Webhook and automatically installed on the Google Cloud Platform (GCP) for dynamic testing. 
The code development is split into Front End and Back End Development to ensure an DevOps way of working with the Front End using HTML/CSS/JS and the Back End using Java and Spring. The data is sent between the front and back end development to ensure information is continuously passed between the two teams, so that the method of working is iterative. 
The design of the Jenkins pipeline job means that if a previous build stage fails, the entirety of the job will fail, providing developers detailed information about where the error has occurred.

















































