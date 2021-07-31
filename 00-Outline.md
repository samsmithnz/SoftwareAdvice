# SoftwareAdvice Outline

## Purpose: share best practices and focus teams on how to be really successful with software development
These are my personal views and do not reflect my employer

## Main points:
- Keep it simple stupid: complexity will come - don't intentionally add complexity.
- Everytime a developer is clever, an atrocity is committed: Keep it simple. Minimize RegEx, XSLT, or Linq, as it's very difficult to maintain/understand later. 
- Software is too complicated (don't add middleware you *might* need)
- Unit testing is important, but most misunderstand it. 
- DevOps/Agile is mostly about culture and behavior change, not tools - but most organizations butcher it to match 'their' process, instead of adapting to DevOps best practices

## Where code falls apart (Agile/DevOps/etc). 

  1. Creating the product
    1. DevOps & Agile
      1. Creating time on Backlog for technical debt and continuous improvement
    1. Code analysis
    2. Code Reviews
    3. Agreeing on formatting - using tools (EditorConfig) to take the opinion out of development
    1. Tools and technologies
    1. Monitoring for feedback
    1. Technology. When to use microservices. When not to. When to use containers. What language to use.
    2. Middleware. Frameworks. Packages. DI. Entity framework


## Managing technical debt

we need to understand what we have. What projects are older, what projects have risky/old technology. We need to catalog all applications



## Cloud Native
- VM's are not cloud native. If you are deploying VM's in 2021 for a new application, you are failing the cloud
- Multiple clouds have resilency, but also double the cost, financially, training, time, and complexity. Don't underestimate this. Don't think that Terraform makes you instantly multicloud. 

## Personal development/ Career planning

1. What do you like doing? What do you not like doing?
2. Where is your dream employer? What is your dream project? 


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
