# Postman API Automation Integration with GitHub Actions #

This repository is a demonstration for POC for integrating postman tests with Github actions. The tests are written in Postman and they are executed on the VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch. We can also execute the project manually using workflow_dispatch.The project runs on a sceduled time with the help of cron jobs.

The HTML reports are archived and kept in the archive section for the team to download it. Along with that they can view the report directly from the github page : https://titun033.github.io/Phoenix-InWarranty-Flow/ .
The latest report is mailed to the team members using Gmail SMTP.

## About Me ##
Hi, This is Titun Chakraborty. I have 12 years of experience in QA and 9 years in Test Automation and DevOps. My skillset include UI Automation with Selenium WebDriver, PLaywright and for API Testing I use Rest Assured, Postman and Newman.
You can connect with me @: (https://www.linkedin.com/in/titun-chakraborty-0aa14077/)

## Test Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge-Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github secrets

# Tech Stack #
1. Postman
2. NodeJS(v24)
3. Newman
4. Newman-reporter-htmlextra
5. Github-actions
6. Gmail SMTP
7. Github pages
8. CSV For Data Driven Testing
9. AWS- EC2 for Self hosted github runner

## GitHub Pages ##
We can directly view the latest test report of the Postman Test at the Github Page Link: https://titun033.github.io/Phoenix-InWarranty-Flow/

## HTML Report ## 
The report will be created in the Newman folder
![Postman Report](https://raw.githubusercontent.com/Titun033/Phoenix-InWarranty-Flow/static-content/Newman-report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json #Collection File
├─ QA.postman_environment.json #Environment File
└─ testData.csv #TestData File

```

## How to run the Project? ##
We can run the project on our local, for that:
1. Clone the project on Local system: ``` https://github.com/Titun033/Phoenix-InWarranty-Flow.git ```
2. Install Nodejs and npm from: ``` https://nodejs.org/en ```
3. Install Newman using: ``` $ npm install -g newman ```
4. Install Newman-reporter-htmlextra using: ```  npm install -g newman-reporter-htmlextra ```
5. Run the newman command: 
6.          $  newman run 'Inwarranty-flow Collection.postman_collection.json' \
            -e 'QA.postman_environment.json' \
            -d testData.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html



