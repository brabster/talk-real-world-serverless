## How big is a function?

Fewer complex functions or more simple functions?

- It Depends &trade;

Note:
 - Started with few, complex, in a monorepo
   - hard to follow the code
   - coupling many different kinds of messages and infrastructure
   - change was scary with far-reaching effects
 - Ended up with many simple functions grouped into a repo per component
   - much easier to understand code in each Lambda
   - harder to understand where lambdas effectively talk to one another via infrastructure
   - all lambdas in a repo working in the same domain
   - possible to scale independently different types of messages
