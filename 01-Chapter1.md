# Chapter 1: DevOps

Let's talk about DevOps, or "DevOops".

## Automated testing
Automated testing is usually the first challenge in implementing DevOps. Resistance is common from the QA manager/team, who misunderstand that the point of automation is not to replace their jobs - it's to replace the long regression testing phases. QA can now focus on the latest changes, and be confident that their previous changes are being tested.

With proper automated testing and a well balanced test pyramid, (no, functional tests are not the first stop, start with your mocked unit tests first), an entire regression test can be run quickly (measured in minutes, not days). You will get this wrong - a lot. That is ok, and is why we track the core DevOps metric "Change failure rate". When we find something we missed (and again, this is the role of everyone on the team, not just QA), create a new test that covers that scenario.

![TDD](assets/TDDAndBridges.png "TDD and bridges")

## Database DevOps
Number 2 issue is data. Database DevOps is hard, as you fundamentally have to change the way you think about managing data. The crux of this comes down to the concept of destructive and non-destructive changes.

- A destructive change is anything that changes a column or table name or type. 
- A non-destructive change is anything additive, adding a new column or table - that does not affect the rest of the database. Note: This assumes that the team is not using "SELECT \*" statements. 

Essentially you want to avoid destructive changes as much as possible. This is hard for DBA's, as the implication is that the focus changes from performance and a 'clean' database schema, to performance and uptime. For example, editing a column name is forbidden. Instead, you should add a new column and a migration from one column to another. Your consuming service only needs to use the new column.

## Infrastructure as Code
Number 3 is Infrastructure as Code. This is where the cloud comes in. Having your entire environment be scriptable is key to meeting one of the DevOps core high performing metrics, Mean Time To Restore (MTTR). This also allows you to create new test environments easily. This isn't always about containers (we will talk about these in a another chapter)

## Feature Flags/Toggles
Not always recognized a being critical to DevOps - but if you want to continually deploy to production, you can't do this without Feature Flags. Feature Flags also help to battle environment sprawl. Have 5-7 environments? (Dev, intergration, test, qa, staging, prod?) Why? What do those middle layers give you? It's like adding 3 different types of lettece in a sandwich - the resulting sandwich is not better or worse. With Feature Flags you can release more WIP into production with the feature disabled for the majority of users. This means we need less environments - which helps with another core DevOps metric: Lead Time For Changes.
