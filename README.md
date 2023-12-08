# PhontenotPhitness

This repo contains: 
1. A MySQL 8 container for obvious reasons
2. A Python Flask container to implement a REST API
3. A Local AppSmith Server

Project document link: https://docs.google.com/document/d/1Q2k__c15uEunEtPmtkhojBu4sp9V8oPYD8Wxzzfk-o0/edit 

## How to setup and start the containers
**Important** - you need Docker Desktop installed

1. Clone this repository.  
1. Create a file named `db_root_password.txt` in the `secrets/` folder and put inside of it the root password for MySQL. 
1. Create a file named `db_password.txt` in the `secrets/` folder and put inside of it the password you want to use for the a non-root user named webapp. 
1. In a terminal or command prompt, navigate to the folder with the `docker-compose.yml` file.  
1. Build the images with `docker compose build`
1. Start the containers with `docker compose up`.  To run in detached mode, run `docker compose up -d`.



# Project Documentation
The project structure consists of 4 primary packages: 
- db
- flask-app
- secrets
- thunder-tests

The db package creates the database of the project. It also creates all the tables that we use for the project. I.e: the personas tables, and any other relationship tables needed based off of the ER diagram in the project document. This code is written in mySQL. 

The flask-app package consists of the necessary python code to handle all the routing for the application. Within the flask-app package, there is an app.py file that creates the application. In the src package, there consists of 4 additional packages each representing a persona of our application. The four personas are: 
- admin: which has all privileges
- coach: which has privileges over athletes
- athletes: which are connected to coaches
- users: basic users not connected to anyone

Within these packages, the code exists that handles all the routes for the personas. A detailed REST API matrix of all the routes that exist in the project lies on pages 14-15 of the project document. 





