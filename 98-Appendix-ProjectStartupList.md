## Project setup checklist

1. Start with an idea
2. Choose a language(s) (C#)
3. Choose an IDE (Visual Studio)
4. Choose a cloud (Azure) 
    1. [ ] What architecture will we use (containers/PaaS/VM scalesets) (the answer should NOT be VM's)
    2. [ ] What is the plan for resilency
    3. [ ] What is the plan for backups 
5. Choose a DevOps platform (GitHub)
    1. [ ] Create an organization
    2. [ ] Create a repo
    3. [ ] Setup branch rules/policies (require a code review)
6. Creating the new/empty project
    1. [ ] Setup basic CI
    2. [ ] Creating basic empty projects (Rest API, Website, etc)
    3. [ ] Creating basic automated test projects - to prove that we are deploying working code 
      1. [ ] unit/integration tests 
      2. [ ] smoke/functional tests
      3. [ ] code coverage
    5. [ ] Add editor config file (to take the opinion out of code styling)
    6. [ ] Add infrastructure as code to deploy to each needed environment (Dev, QA, Prod?)
7. Back to GitHub
     1. [ ] Setup dependabot to automatically update dependencies
     2. [ ] Setup security to check for secrets and unsafe dependency
     3. [ ] Setup basic CD, to deploy to each cloud environment, with smoke tests and environment approvals as needed 
8. Project planning
     1. [ ] Set goals/roadmap. What does Alpha/Beta/GA look like?
     2. [ ] Create Epics
     3. [ ] Create Features
     4. [ ] Create PBI/ User Stories
