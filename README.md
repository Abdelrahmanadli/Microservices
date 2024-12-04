Step 1: Version Control & Project Setup:

-Created a github repo containing the .gitignore file and readme.md

-Cloned the repo on my device *git clone https://github.com/Abdelrahmanadli/Microservices*

-Made sure to commit changes as much as possible * git add .
git commit -m 'Initialize project with README and .gitignore'*


Step 2: Database Integration
-Downloaded SQL express and SSMS from " https://www.microsoft.com/en-us/sql-server/sql-server-downloads?msockid=3245596d3aa2612a2cdc4d103bea601c”

-Downloaded adventureworks2022.bac and attached it to the database

-Ran *dotnet new webapi* to build a .net project

-Added *"ConnectionStrings": {
    "DefaultConnection": "Server=DESKTOP-B1HEDNI\\SQLEXPRESS;Database=AdventureWorks2022;Trusted_Connection=True;TrustServerCertificate=True;" 
  },* to the appsetting.json file
  
-Locally installed the EF package * dotnet new tool-manifest

dotnet tool install dotnet-ef
dotnet tool restore
dotnet ef –version
dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameworkCore.Tools* to install all the dependencies

-Ran the * dotnet ef dbcontext scaffold "Server=DESKTOP-B1HEDNI\SQLEXPRESS;Database=AdventureWorks2022;Trusted_Connection=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer* command in the terminal to initiate the API endpoint connection


Step 3: Microservices Architecture with Docker

-installed Docker Desktop

-created a file called *Dockerfile*, with it’s respective code

-Ran * docker pull mcr.microsoft.com/mssql/server* in the docker desktop terminal

-Created a file called *docker-compose.yml*, with it’s respective code

-Ran the *docker-compose up --build* command in the terminal to make a build in the docker file and it showed up on the docker desktop


Step 4: Set Up CI/CD Pipeline with Jenkins

-installed Jenkins

-Created a jenkinsfile in github and built a new item using pipeline that connects to the github to run the jenkinsfile.

-Made a Successful Build


Step 5: Documentation
-Made Documentation

-installed swagger by using the following commands

-* npm install -g swagger* to initially install it

-* dotnet add package Swashbuckle.AspNetCore* to add the required package

-*dotnet run* to run the app and obtain the port number

- *http://localhost:5130/swagger/index.html* to access the swagger site
