# Chapter 1: DevOps

Let's talk about DevOps, or "DevOops".

## Automated testing
Number 1 problem/challenge is automated testing. Resistance is common from the QA manager/team, who misunderstand that the point of automation is not to replace their jobs - it's to replace the long regression testing phases. With proper automated testing and a well balanced test pyramid, an entire regression test can be run quickly.

![TDD](/images/TDDAndBridges.png "TDD and bridges")

## database DevOps
Number 2 issue is data. DevOps on database is hard, as you fundamentally have to change the way you think about managing data. The crux of this comes down to the concept of destructive and non-destructive changes.

- A destructive change is anything that changes a column or table name or type. 
- A non-destructive change is anything additive, adding a new column or table - that does not affect the rest of the database. Note: This assumes that the team is not using "SELECT \*" statements. 

Essentially you want to avoid destructive changes as much as possible. This is hard for DBA's, as the implication is that the focus changes from performance and a 'clean' database schema, to performance and uptime. For example, editing a column name is forbidden. Instead, you should add a new column and a migration from one column to another. Your consuming service only needs to use the new column.
