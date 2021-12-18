# The Cloud

It doesn't matter what cloud you use, they are mostly equivalent, but keep in mind

1. Your current environment: If you are using mostly Microsoft products and Active Directory, Azure makes sense as the best cloud. If you are mostly using Google products, GCP makes sense. For everyone else, AWS makes sense. 
2. Your team: asking a team with experience with Azure to became AWS experts (and vice versa) is going to cause pain - and attrition. Make sure you approach this with care. "Are you interested in working with a second cloud"?
3. Multiple clouds: There is no technology out there that makes multiple clouds easier to adopt. There is a significant amount of administration, security, governance and setup that needs to happen for every cloud. Containers don't enable it, terraform doesn't enable it. They help - but two clouds is still twice the work of one, and three, triple the work of one.

## Cloud native

A very mis-understood term. 
- VM's are not cloud native. If you are deploying VM's in 2021 for a new application, you are failing the cloud test
- Multiple clouds have resilency, but also multiply the financial cost, training, time, and complexity. Don't underestimate this. Don't think that Terraform or containers makes you instantly multicloud.
