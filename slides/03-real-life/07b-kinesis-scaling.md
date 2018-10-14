## Mismatching Capacity

One function instance per Kinesis partition...

...make sure functions are fast!

## How big is a function?

Fewer complex functions or more simple functions?

...it depends &trade;

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

Note:
 - Busy systems delay quiet ones
 - Autoscaling means you can insert coins to continue
   - Fixes a short burst, buys time for longer-term fixes
 - Stuff that autoscales but depends on stuff that doesn't doesn't autoscale!
 - Can roll your own autoscaling, but not pretty
 - Complex code and two DynamoDB accesses per message meant we had a slow function
 - In our design, busy systems delayed message processing for quiet systems
