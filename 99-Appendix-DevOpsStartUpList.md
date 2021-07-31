## steps to success
Behavior's to successful DevOps

1. **DevOps foundation**
    1. **Why DevOps?** Explain the benefits, get everyone on the same page.
    1. **What is DevOps** - get everyone on the same page
    1. **Executive support** - get budgets/ time/ buyin from top to bottom.
    1. **Team POC** - identify the right team/project to test these ideas. A smaller project/single team is easier than a large project/many teams.
    1. **Construct the Team** - ensure we have the right people. Do we have a security person? a developer? ops? product manager/owner? a DBA? QA? Who else needs to be involved? 
    1. **Value Stream Mapping** - understand the pain points in our current process. How long does it take to change a line of code and release it to our end users? Where are the bottlenecks? What processes are manual (and can be automated)?
1. **Dev**
    1. **Source Control** - Create a repository in GitHub. Create a backlog of issues and prioritize them. Setup security.
    1. **Branching strategy** - decide on a branching strategy. Hint: Simplier is better, you can always add complexity later. Ideally a main branch with feature branches is best. Warning: This could be a holy war, keep this timeboxed and scoped. Have someone pull rank if needed. This is not a good place to experiment, it just leads to pain. KEEP IT SIMPLE. 
    1. **Coding Standards** - What standards should the code be following? Ideally automation would be best here (e.g. an editorconfig file). Move the opinion from the code review er to an automated system to reduce team conflit 
    1. **Code Analysis** - what code analysis tools will we use to ensure quality? CodeQL? SonarCloud? Using this earlier will keep a handle on technical debt. Warning: Running this on existing projects will uncover hundreds, if not thousands of issues and overwhelm the team. Consider ignoring the first batch of issues on an existing project, or everything non-critical. 
1. **CI**
    1. **Branch Policies** - When we create a PR, what do we need to merge the feature branch back to main? A successful build? Tests? Code review? manager approver? Try to minimize the number of people involved. If you need a DBA, senior director, security guy, and architect to approve every change, your process benefits will be reduced. 
    1. **Pull Requests** - Not muct to setup here after branch policies and branch strategy is done. A good time to remind the team that pull requests, like branches, should be short lived, hanging around for days, not months. Have the team use PR's for work in progress and use draft PR's to help them develop the feature
    1. **Testing Strategy** - Unit tests are critical. If you can't get feedback on a change in seconds or minutes - then your application is in trouble. Have a good balance of unit, integration and functional tests. Include performance and load tests too!
1. CD
    1. Continuous Delivery
    1. Continuous Deployment
1. CM
    1. DevSecOps
    1. Continuous learning
