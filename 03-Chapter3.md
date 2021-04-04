# Architecture

> "Whenever a developer thinks they are being clever, they commit an atrocity"

## The curse of Microservices and SOA
Is your project strategic or is it a line of business application? Does it a major revenue generator for your company? Does your project have 10's of thousands to millions of users? With the rise of Microservices, it's becoming a more common strategy - but more often than not, it will fail. Why?
1. Microservices require dedicated teams. If the team is balancing multiple applications, chances are they don't have the right allocation/bandwidth to make the microservice successful.
2. There is no point creating a microservice for a single instance application. If it doesn't need scale or uptime, it doesn't need resilency at this level. 
3. You should never start a project with a design that requires many microservices. The recommendation is, instead, to start building your monolith (which isn't always a negative output), and as you need to, as you have pieces that need scale and independence, you break off pieces and turn them into a microservice.

## The curse of Middleware
Many projects are overly-complicated and contain middleware that is unnecessary. There are a number of reasons this happens - some of it is the culture in our industry, where many feel they need to prove they are smart with their complex system. But the reality is a good system is a simple one. A good system is one that is easy to maintain, scale and runs at a high performance. A poor system is a complex one that is difficult to maintain and teams are scared to make changes and deploy those changes.

When you add middleware, really ask the question: What problem does this solve? Is the problem it solves one I have today - or a perceived problem in the future? 
