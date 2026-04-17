# postman API automation Integration with Github Actions #

This repository is a demonstration for poc for Integration postman tests with github actions. The tests are written in postman and they are executed on the virtual machine with the help of newman and newman-reporter-htmlextra.
This project github actions will trigger the project execution on every push to the main branch. You can also execute the project manually using workflow_dispatch .The project runs on schedule time with the crone job.

The html report is the archieved and kep under artifact section for the team to download it.Along with that they can view the report directly from the github page: https://ramita123.github.io/Phoenix-InWarranty-Flow-Collection-Files/
The latest report is mailed to the team members using gmail smtp.

## About me ##
Hi, My name is Ramita . I have 7.3 years of experince in Testing. My skill set includes UI Automation with selenium web driver and for API testing I use Rest assured and postman.


## Testing Coverage ##
1. Happy Flow Testing
2. Negative testing and edge case testing
3. Token Testing
4. Data driven testing with csv
5. Schema validation
6. Secrets Management with github secrets 

# Teach Stack #
1. Postman
2. nodejs 22
3. newman
4. newman-reporter-htmlextra
5. github actions
6. gmail smptp
7. github pages
8. CSV for data driven testing
9. AWS ec2 instance for self hosted github runner

#HTML Report #
![Postman Report](https://github.com/ramita123/Phoenix-InWarranty-Flow-Collection-Files/blob/static-content/newman-report.png)

## Project Struture ##
phoenix inwarranty flow
├─ InWarrenty flow Copy.postman_collection.json  # collection file
├─ phoenix_URL.postman_environment.json # environment file
├─ testdata.csv  # test data filr

# Github Pages #
you can directly view the latest test report of the postman test at the Github page: https://ramita123.github.io/Phoenix-InWarranty-Flow-Collection-Files/

# How to run the project ? #
you can run the project on your local system for that 
1. clone the project on your local system : https://github.com/ramita123/Phoenix-InWarranty-Flow-Collection-Files.git
2. install nodejs and npm from https://nodejs.org/en/download
3. intsall newman ``` npm install -g newman ```
4. install newman-reporter-htmlextra ```npm install -g newman-reporter-htmlextra```
5. run the newman command :
   ```
          newman run 'InWarrenty flow Copy.postman_collection.json' \
            -e phoenix_URL.postman_environment.json \
            -d testdata.csv \
            -r cli,htmlextra \
            --reporter-htmlextra-export ./newman/index.html
   ```


