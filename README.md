# Postman API Automation Integration with Github Actions #

This Repository is a demonstration for POC for integrating Postman tests with Github Actions. The tests are written in Postman and they are executed on the VM with the help of Newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every PUSH to the main branch. You cab also execute the project manually using workflow_dispatch. The project runs on a schedule time with the help of the CRON job.

The HTML report is archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the Github page :https://yousuf2106.github.io/Phoenix-Inwarranty-Flow/.

Rhe Latest Report is mailed to the team members using GMAIL SMTP.

## About me ##
Hi my name is Yousuf Shareef. I have 8 years of experience in software testing. My Skillset includes UI Automation with Selenium WebDriver, Cypress, Playwright and for API testing i use Rest Assured and Postman.
You can connect with me over: [LinkedIn](https://www.linkedin.com/in/yousuf-shaik-717b2b28/)

 ## Testing coverage ##
  1. Happy Flow Testing
  2. Negative Tetsing and Edge case Testing
  3. Token Testing
  4. Data Driven Testing with CSV
  5. Schema Validation
  6. Secrets Management with Github Secrets

## Tech Stack ##
1. Postman
2. Nodejs 22v
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for data driven testing
9. AWS- EC2 instance for self-hosted github runner.

## Githu Pages ##
you can directly view the latest report of the Postman tests at the Github Page link : https://yousuf2106.github.io/Phoenix-Inwarranty-Flow/

## HTML report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/Yousuf2106/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##

```
Phoenix Inwarranty Flow
├─ Inwarranty-flowClean.postman_collection.json  #Collection file
├─ QA.postman_environment.json  #Environment file
└─ testdata.csv  #Test data file

```

## How to run the project ##
You can run the project on your local system for that:
1. Clone the project on local system:https://github.com/Yousuf2106/Phoenix-Inwarranty-Flow.git
2. Install Nodejs and NPM from https://nodejs.org/en
3. Install Newman using: ``` npm install -g newman```
4. Install Newman-reporter-htmlextra using : ```npm install -g newman-reporter-htmlextra```
5. Run the Newman command :
  
```
           newman run Inwarranty-flowClean.postman_collection.json \
          -e QA.postman_environment.json \
          -d testdata.csv \
          -r cli,htmlextra \
          --reporter-htmlextra-export ./newman/index.html

```



 
