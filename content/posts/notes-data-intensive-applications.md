---
title: "Notes: Designing Data Intensive Applications"
date: 2021-07-01T23:17:38-06:00
draft: false
---
## Chapter 1 (July 1st, 2021)
### Initial questions:

- How do you ensure that the data remains correct and complete, even when things go wrong internally?
- How do you provide consistently good performance to clients, even when parts of your system are degraded?
- How do you scale to handle an increase in load? What does a good API for the service look like?

### Three main concerns:

- A.) Reliability - continuing to work correctly, even when things go wrong.
- B.) Scalability
- C.) Maintainability

### A.) Reliability
We can't completely eliminate the threat of a fault so instead focus on designing systems that prevent faults from 
causing failures.

The Netflix Chaos Monkey [1]

Large cloud platforms, such as AWS, prioritize flexibility and elasticity over single-machine reliability. This can cause
unexpected outages - hence a move toward software that is itself fault tolerant.

[1]: https://netflix.github.io/chaosmonkey/